---
title: "Collections sort with lambda expressions"
excerpt: "collections-sort-with-lambda-expressions"
sitemap: true
permalink: /sample-codes/collections-sort-with-lambda-expressions/
author_profile: true
---
[`Interface Comparator <T>`](https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html) is also a functional interface and can be used with lambda expressions.

~~~~
Collections.sort(studentList, Comparator.comparing(Student::getCgpa).reversed().thenComparing(Student::getFname).thenComparing(Student::getId) );

for(Student st: studentList){
System.out.println(st.getFname());
      }
      ~~~~
      
      This code was used [at this challenge](https://www.hackerrank.com/challenges/java-sort/).
