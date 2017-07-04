---
title: "Exeption handling"
excerpt: "exception-handling"
sitemap: true
permalink: /sample-codes/exception-handling/
author_profile: true
---
Handling of exceptions is an important part of codeing especially when we code for real life data and real users.<br>


~~~~
 class MyCalculator {
     public int power (int n, int p) throws Exception {
         
         if(n < 0 || p < 0)
              {throw new Exception("n and p should be non-negative");}
         else {
                 return ((int) Math.pow((double) n,(double) p));
             }
     }
     
     
 }
 ~~~~

~~~~

	public void add(int index, E element ) 
	{
		// TODO: Implement this method
		if(index>size()||index<0){throw new IndexOutOfBoundsException("Error: index out of bound!");}
		if(element==null){throw new NullPointerException("Error: element is null!");}
		LLNode counter=head;
		for (int i=0;i<index+1;i++){
			counter=counter.next;
		}
		counter.prev.next=new LLNode();
		
		//the new node
		counter.prev.next.data=element;
		counter.prev.next.next=counter;
		counter.prev.next.prev=counter.prev;
		counter.prev=counter.prev.next;
		size++;
		
	}
  ~~~~

