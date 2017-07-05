---
title: "Collections.sort with lambda expressions"
excerpt: "collections-sort-with-lambda-expressions"
sitemap: true
permalink: /sample-codes/collections-sort-with-lambda-expressions/
author_profile: true
---
The [`sort(List<T> list, Comparator<? super T> c) method of the Collections class`](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html){:target="_blank"} enables to use lambda expressions in sorting as
[`Interface Comparator <T>`](https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html){:target="_blank"} 
is a functional interface and can be used with lambda expressions.
<br>


~~~~

Collections.sort(studentList, Comparator.comparing(Student::getCgpa).reversed().thenComparing(Student::getFname).thenComparing(Student::getId) );

for(Student st: studentList){
System.out.println(st.getFname());
      }
      
~~~~
  
This code was used [at this challenge](https://www.hackerrank.com/challenges/java-sort/).
