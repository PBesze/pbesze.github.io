---
title: "Implementing the Comparator interface"
excerpt: "implementing-the-comparator-interface"
sitemap: true
permalink: sample-codes/implementing-the-comparator-interface/
author_profile: true
---
Implementing abstract classes and interfaces is an effective tools for the functionality of multiple inheritance.
In this simple generaly known example Checker class implements [`Interface Comparator <T>`](https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html), that players are compared by score and name: 
	
~~~~
class Checker implements Comparator<Player>{
    @Override
    public int compare(Player player1, Player player2){
        if (a.score == b.score){
            return player1.name.compareTo(player2.name);
        } else {
            return player2.score - player1.score;
        }
    }
}
~~~~
