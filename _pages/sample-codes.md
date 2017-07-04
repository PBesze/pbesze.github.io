---
title: "Sample-codes"
excerpt: "Sample-codes"
sitemap: true
permalink: /sample-codes/
author_profile: true
---

**Java Arraylist**<br>
	To solve this task on hackerrank.com:
	https://www.hackerrank.com/challenges/java-arraylist
	
	`
  import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
                       Scanner in = new Scanner(System.in);
       
        int m=0;
        
        List<Integer> row = new ArrayList<Integer>();
        List<List<Integer>> array = new ArrayList<List<Integer>>();
         int n = in.nextInt();
        for(int i = 0;i<n;i++){
            //input rows
           
            m = in.nextInt();
            for (int j=0;j<m;j++){
                row.add(in.nextInt());
        
            }
        
            array.add(row);
            row= new ArrayList<Integer>();
        }
        n = in.nextInt();

      
        int x =0;
        int y=0;
        for(int i = 0;i<n;i++){
            x = in.nextInt();
            y = in.nextInt();
            try {System.out.println( array.get(x-1).get(y-1) );}
            catch (Exception e){System.out.println("ERROR!");}
        }

    }
}
	`
	
	[**Implements Comparator**] (https://pbesze.github.io/sample-codes/implements-comparator)
  <br>
	

**Following pseudocode** <br>


**RegEx** <br>

**Exception handlig** <br>

	
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
