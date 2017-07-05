---
title: "Queries in arraylist"
excerpt: "queries-in-arraylist"
sitemap: true
permalink: /sample-codes/queries-in-arraylist/
author_profile: true
---

To solve [a task on hackerrank.com](https://www.hackerrank.com/challenges/java-arraylist){:target="_blank"} I wrote the following code:


~~~~
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        List<Integer> row;
        List<List<Integer>> array = new ArrayList<List<Integer>>();               
        Scanner in = new Scanner(System.in);
        //input the number of rows
        int n = in.nextInt();
        int m=0;
        
        for(int i = 0;i<n;i++)
        {
        //input rows to Arraylist
            m = in.nextInt();
            row= new ArrayList<Integer>();
            for (int j=0;j<m;j++)
            {
                row.add(in.nextInt());
            }
        
            array.add(row);
            
        }
        //input the number of selections
        n = in.nextInt();

         //selecting elemnts and catch the requested exception
        int x =0;
        int y=0;
        
        for(int i = 0;i<n;i++)
        {
            x = in.nextInt();
            y = in.nextInt();
            try {System.out.println( array.get(x-1).get(y-1) );}
            catch (Exception e){System.out.println("ERROR!");}
        }

    }
}
~~~~
