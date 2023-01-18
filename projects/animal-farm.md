---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "Animal Farm"
date: 2022
published: true
labels:
  - C
  - C++
  - Object Oriented Programming
summary: "Animal Farm is a series of labs intended to teach the basics of C and C++ as the code evolves over a series of requirements. It's also intended to introduce good Software Engineering practices."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

Animal Farm is a project intended to teach the basics of C and C++ in EE 205 or Object Oriented Programming at the University of Hawaii. Every week or two, a new version of Animal Farm was expected to be pushed to Github with more advanced requirements each time. Throughout the course of the project, I was able to learn how to refactor and improve source files. Initially, we wrote Animal Farm in C and later used CLion to refactor the code to represent the animals on the farms as objects. Towards the latter half of the project, I was introduced to README files, makefiles, and Doxygen notation. The different versions of Animal Farm were as follows:
  * Animal Farm 0: An array-based database of cats, where each attribute is an array.
  * Animal Farm 1: An array-based database of cats, where each a cat's attributes are collected in a struct.
  * Animal Farm 2: A procedural singly linked-list database of cats, where each cat is an object.
  * Animal Farm 3: A collection class that implements a singly linked database of Animal objects using: an abstract List, a concrete SinglyLinkedList, and generic Node. Added an abstract Animal (which also inherits from Node) & Mammal to the Cat object model.
