
# Introduction to Design Patterns

## What is a Design Pattern?

Design patterns are reusable solutions to common problems that occur in software design. They represent best practices evolved by experienced software developers over time. The concept was popularized by the "Gang of Four" (Gamma, Helm, Johnson, and Vlissides) in their 1994 book "Design Patterns: Elements of Reusable Object-Oriented Software."

Think of design patterns like proven recipes for solving common coding problems. Just as chefs use recipes to make dishes consistently delicious, programmers use design patterns to write better code without reinventing solutions.




## Why Use Design Patterns?

- Provide a shared vocabulary for developers
- Represent proven solutions to recurring problems
- Help avoid reinventing the wheel
- Make code more maintainable and flexible
- Facilitate communication between team members

## Pattern Elements

1. **Pattern Name**: What we call the pattern (like a recipe name)
2. **Problem Description**: When to apply the pattern and in what context, When you should use this pattern (like knowing when to bake vs. fry)
3. **Solution**: How to implement the pattern (the actual recipe steps)
4. **Consequences**: What happens when you use this pattern (the taste and nutrition of the dish)




## Design Patterns Types

There are 23 classic design patterns divided into three categories:

### 1. Creational Patterns

These patterns deal with object creation mechanisms, trying to create objects in a manner suitable to the situation.

These help you create objects in smart ways.

**Real-life example**: Think of a car factory. Different factories (patterns) create different types of cars in different ways.


1. **Abstract Factory**: Creates families of related objects without specifying concrete classes
2. **Builder**: Separates object construction from its representation
3. ***Factory Method***: Creates objects without specifying the exact class to create
4. **Prototype**: Creates new objects by copying existing objects
5. ***Singleton***: Ensures a class has only one instance and provides a global point of access

### 2. Structural Patterns

These patterns deal with object composition, forming larger structures from individual objects.

1. **Adapter**: Allows incompatible interfaces to work together
2. **Bridge**: Separates an abstraction from its implementation
3. **Composite**: Composes objects into tree structures to represent part-whole hierarchies
4. **Decorator**: Attaches additional responsibilities to objects dynamically
5. **Facade**: Provides a simplified interface to a complex subsystem
6. **Flyweight**: Minimizes memory usage by sharing as much data as possible with similar objects
7. **Proxy**: Provides a surrogate or placeholder for another object to control access to it

### 3. Behavioral Patterns

These patterns focus on communication between objects, how objects interact and distribute responsibility.

1. **Chain of Responsibility**: Passes a request along a chain of handlers
2. **Command**: Encapsulates a request as an object
3. **Interpreter**: Implements a specialized language
4. **Iterator**: Accesses elements of a collection sequentially without exposing its representation
5. **Mediator**: Defines simplified communication between classes
6. **Memento**: Captures and restores an object's internal state
7. **Observer**: Defines a one-to-many dependency between objects
8. **State**: Allows an object to alter its behavior when its internal state changes
9. **Strategy**: Defines a family of algorithms and makes them interchangeable
10. **Template Method**: Defines the skeleton of an algorithm, deferring some steps to subclasses
11. **Visitor**: Separates an algorithm from the object structure on which it operates

## Example: Singleton Pattern


```java
public class ScoreCounter {
    // There can only be one score counter in the whole game
    private static ScoreCounter instance;
    
    // The score starts at zero
    private int score = 0;
    
    // Nobody else can create a score counter
    private ScoreCounter() { }
    
    // Everyone must use this method to get the one score counter
    public static ScoreCounter getScoreCounter() {
        if (instance == null) {
            instance = new ScoreCounter();
        }
        return instance;
    }
    
    // Methods to use the score counter
    public void addPoints(int points) {
        score += points;
    }
    
    public int getScore() {
        return score;
    }
}
```

This ensures everyone in the game is looking at the same score, not different copies that get out of sync.


This pattern ensures that a class has only one instance and provides a global point of access to it.

## Connection to Other Topics

Design patterns are closely related to object-oriented programming principles (encapsulation, inheritance, polymorphism) and are fundamental to good software architecture and design.
