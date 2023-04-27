---
layout: essay
type: essay
title: "Building Code Brick by Brick"
date: 2023-04-26
published: true
labels:
- Design Patterns
- Efficient
- Programming Techniques
---
## Legos?

<div class="text-center p-4">
  <img width="500px" class="img-thumbnail" src="../img/lego.jpg" >
</div>

Once you begin to program, it can often feel like you're playing with a bunch of Legos. Legos can be described as standardized blocks that can be combined using a simple, yet effective set of instructions to create various structures. Like the Lego bricks, design patterns play a similar role in the grand scheme of a large program. A design pattern is a general, proven, repeatable solution to a commonly occurring problem in software design. By utilizing the design patterns in different situations, scalable, reusable, easily understood, maintained, and more efficient code can be used to create various solutions.

## Bricks Galore!

<div class="text-center p-4">
  <img width="500px" class="img-thumbnail" src="../img/diff-lego.jpg" >
</div>

There are a total of about 3764 unique Lego pieces that can be pieced together in different combinations. Similarly, there are different classifications of design patterns that can be used to solve different problems. Design patterns can be classified into three main categories: creational patterns, structural patterns, and behavioral patterns. Creational patterns create objects and classes that increase flexibility and reuse of existing code. Structural patterns organize code and classes into larger structures so they are easier to maintain and understand. Behavioral patterns manage the interactions between objects and classes.

## My Lego Builds

<div class="text-center p-4">
  <img width="500px" class="img-thumbnail" src="../img/lego-build.jpg" >
</div>

For the past couple of weeks, my team and I have been developing a website for UH Manoa musicians to create and connect through local jam sessions called [jamb-UH-ree](https://github.com/jamb-uh-ree). Within this project itself, there are many different design patterns.

### Singleton Design Pattern Example
A type of creational pattern is the Singleton pattern. In this pattern, a “global variable” is created and can be accessed from anywhere in the project. Many Singleton patterns exist within the codebase since each collection was exported to the rest of the project, making it easier to manipulate them from the methods in the client-side code. Specifically below is an example from the Gigs.js file, which shows the Gigs Collection.
```
class GigsCollection {
  constructor() {
    // The name of this collection.
    this.name = 'GigsCollection';
    // Define the Mongo collection.
    this.collection = new Mongo.Collection(this.name);
    // Define the structure of each document in the collection.
    this.schema = new SimpleSchema({
      title: { type: String, optional: false },
      image: { type: String, optional: false },
      date: { type: Date, optional: false },
      skillLevel: { type: String, allowedValues: ['Beginner', 'Intermediate', 'Advanced'], optional: true },
      genres: { type: Array },
      'genres.$': { type: String, optional: true },
      instruments: { type: Array, optional: true },
      'instruments.$': { type: String },
      venue: { type: String, optional: true },
      about: { type: String, optional: true },
    });

    // Ensure collection documents obey schema.
    this.collection.attachSchema(this.schema);
    // Define names for publications and subscriptions
    this.userPublicationName = `${this.name}.publication.user`;
    // this.adminPublicationName = `${this.name}.publication.admin`;
  }
}

export const Gigs = new GigsCollection();
```
This is a Singleton pattern because the Gigs variable is an instance of the GigsCollection class and it is exported. Each time the module is imported, the same instance of the GigsCollection is returned. Thus, there is no way to create another instance of this class from outside of this module. 

## A Note From the Master Builder
As the master builder, I can attest that design patterns are efficient tools that can help other master builders create easy-to-understand code. They provide an easy way to start projects as guidelines instead of starting from scratch. Prior to this essay, I had no clue what design patterns were. This didn’t matter because I implemented a variety of design patterns in the code I wrote for this course and others previously. Now that I am aware of how common and useful they are, I will continue to build my code brick by brick.




