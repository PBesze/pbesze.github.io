---
title: "Following pseudocode"
excerpt: "following-pseudocode"
sitemap: true
permalink: /sample-codes/following-pseudocode/
author_profile: true
---
<br>
In a complicated algorithm it is usefull to write and follow pseudocode as it was done for example in a trie search:<br>
*The task was part of my [Data Structures and Performance course](https://www.coursera.org/learn/data-structures-optimizing-performance){:target="_blank"}*.

~~~~

public List<String> predictCompletions(String prefix, int numCompletions) 
     {
    	 // TODO: Implement this method
    	 // This method should implement the following algorithm:
    	 // 1. Find the stem in the trie.  If the stem does not appear in the trie, return an
    	 //    empty list
    	 // 2. Once the stem is found, perform a breadth first search to generate completions
    	 //    using the following algorithm:
    	 //    Create a queue (LinkedList) and add the node that completes the stem to the back
    	 //       of the list.
    	 //    Create a list of completions to return (initially empty)
    	 //    While the queue is not empty and you don't have enough completions:
    	 //       remove the first Node from the queue
    	 //       If it is a word, add it to the completions list
    	 //       Add all of its child nodes to the back of the queue
    	 // Return the list of completions
    	 Queue<TrieNode > q= new LinkedList < TrieNode >();
    	 List<String> predi= new ArrayList<>();
    	 prefix = prefix.toLowerCase();
 		TrieNode curr=root;
 		
 		//search of the stem
 					for(int i=0;i<prefix.length();i++)
 					{
 						if (curr.getChild(prefix.charAt(i))== null){return predi;}
 						if (curr!=null){
 							curr=curr.getChild(prefix.charAt(i));
 					}}
 		//add stem&childs to the queue
 			if(curr.endsWord()){predi.add(curr.getText());}
 					Set<Character> chars = curr.getValidNextCharacters();
 					for (char next: chars){
							if(curr.getChild(next)!=null)
							{q.add(curr.getChild(next)); }	
							
						}
 					
 		// WHILE the queue is not empty and you don't have enough completions:
 					while (q.size()>0&&predi.size()<numCompletions){
 						
 		//	remove the first Node from the queue
 						curr=q.remove();
 		//  If it is a word, add it to the completions list	
 					if(curr.endsWord()){predi.add(curr.getText());}
 		//  add its children to the queue ---> WHILE
 					chars = curr.getValidNextCharacters();
 					for (char next: chars){
							if(curr.getChild(next)!=null)
							{q.add(curr.getChild(next)); }	
						;}
 					}
 		// return first numCompletions from predi
 					if (predi.size()>0){
 						if(predi.size()<=numCompletions){numCompletions=predi.size();}
 						//System.out.println(predi.subList(0, numCompletions));
 						return predi.subList(0, numCompletions);}
 					
         return Collections.emptyList();
     }
     
  ~~~~
