---
title: "Implements Comparator"
excerpt: "Sample-codes"
sitemap: true
permalink: sample-codes/implements-comparator/
author_profile: true
---

Checker class implements Comparator class, that players are compared by score and name: 
	
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
