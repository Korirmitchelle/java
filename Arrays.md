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
    
### Multidimensional Array

    class Myarray1 {  
    public static void main(String args[]){  
  
    //declaring and initializing 2D array  
    int arr[][]={{1,2,3},{2,4,5},{4,4,5}};  
  
    //printing 2D array  
    for(int i=0;i<3;i++){  
    for(int j=0;j<3;j++){  
      System.out.print(arr[i][j]+" ");  
     }  
    System.out.println();  
    }  
  
    }}
    
## Advantage of Java Array

+ Code Optimization: It makes the code optimized, we can retrieve or sort the data easily.
* Random access: We can get any data located at any index position.


## Disadvantage of Java Array

+ Size Limit: We can store only fixed size of elements in the array. It doesn't grow its size at runtime. To solve this problem, collection framework is used in java.    