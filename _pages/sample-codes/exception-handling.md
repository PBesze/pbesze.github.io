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
