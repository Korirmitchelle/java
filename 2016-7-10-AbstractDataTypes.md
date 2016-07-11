---
layout: post
title: Abstract Data Types
---

# DATA TYPES

A data type is characterized by:
+ a set of values
- a data representation, which is common to all these values, and 
* a set of operations, which can be applied uniformly to all these values

## Primitive Data Types

Java provides eight primitive types:

* boolean, char, byte, short, int, long, float, double

Each primitive type has

* a set of values
- a data representation
+ a set of operations

These are “set in stone”—there is nothing the programmer can do to change anything about them

## Abstract Data Types

An Abstract Data Type (ADT) is:

* a set of values
- a set of operations, which can be applied uniformly to all these values

To abstract is to leave out information, keeping (hopefully) the more important parts

An ADT may be implemented in several different ways.
A complex number might be stored as two separate doubles, or as an array of two doubles, or even in some bizarre way

An ADT must obviously have some kind of representation for its data. The user need not know the representation. The user should not be allowed to tamper with the representation
A solution would be to make all data private.
But if it’s really more convenient for the user to have direct access to the data,
setters and getters would come in handy.

    class Pair {
    private int first, last;

    public getFirst() { return first; }
    public setFirst(int first) { this.first = first; }

    public getLast() { return last; }
    public setLast(int last) { this.last = last; }
    }

Setters and getters should be named by:

* Capitalizing the first letter of the variable (first becomes First), and
- Prefixing the name with get or set (setFirst)
+ For boolean variables, replace get with is (for example, isRunning) 
This is more than just a convention—if and when you start using JavaBeans, it becomes a requirement

Every ADT should have a contract (or specification) that:
* Specifies the set of valid values of the ADT
- Specifies, for each operation of the ADT:
+ Its name
* Its parameter types
- Its result type, if any
+ Its observable behavior

Does not specify:
The data representation
The algorithms used to implement the operations

