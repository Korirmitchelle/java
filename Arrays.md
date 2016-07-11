# ARRAYS

An array is a collection of elements all of the same type
Array objects in Java must be created with the key word new

**Syntax**

     int c[] = new int [12];
Results:
12 integer locations are allocated
They are initialized to 0
(null for reference variables, false for boolean)

## Types of Array in java

There are two types of array.

+ Single Dimensional Array
* Multidimensional Array

### Single Dimensional Array

    class Myarray{  
    public static void main(String args[]){  
  
    int a[]=new int[5];//declaration and instantiation  
    a[0]=10;//initialization  
    a[1]=20;  
    a[2]=70;  
    a[3]=40;  
    a[4]=50;  
  
    //printing array  
    for(int i=0;i<a.length;i++)//length is the property of array  
    System.out.println(a[i]);  
  
    }}  