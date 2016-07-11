---
layout: post
title: Abstraction
---


**Abstraction** is a process of hiding the
implementation details from the user, only
the functionality will be provided to the
user. In other words user will have the
information on what the object does
instead of how it does it.
In Java Abstraction is achieved using
Abstract classes, and Interfaces. 

**Abstract classes** may or may not
contain abstract methods ie., methods
with out body ( public void get(); )
But, if a class has at least one
abstract method, then the class must
be declared abstract.
If a class is declared abstract it cannot
be instantiated.


To use an abstract class you have to
inherit it from another class, provide
implementations to the abstract
methods in it.
If you inherit an abstract class you
have to provide implementations to all
the abstract methods in it.

**Abstract method is a method that is declared as abstract and
does not have implementation.

## Example:

     public abstract class Employee                                               
      {
    private String name;
    private String address;
    private int number;
    public Employee(String name, String
    address, int number)
     {
      System.out.println("Constructing an
    Employee");
      this.name = name;
      this.address = address;
      this.number = number;
    }
    public double computePay()
    {
     System.out.println("Inside Employee
    computePay");
     return 0.0;
    }
    public void mailCheck()
       {
      System.out.println("Mailing a check to
    " + this.name
       + " " + this.address);
     }
    public String toString()
     {
      return name + " " + address + " " +
    number;
    }
          public String getName()
    {
      return name;
     }
    public String getAddress()
     {
      return address;
     }
    public void setAddress(String
    newAddress)
    {
      address = newAddress;
    }
    public int getNumber()
    {
     return number;
    }
    }
    
    
## Inheriting the Abstract Class:

We can inherit the properties of Employee
class just like concrete class as shown
below:

    /* File name : Salary.java */
    public class Salary extends Employee
    {
       private double salary; //Annual salary
     public Salary(String name, String
    address, int number, double
      salary)
     {
       super(name, address, number);
       setSalary(salary);
     }
    public void mailCheck()
    {
       System.out.println("Within mailCheck
    of Salary class ");
       System.out.println("Mailing check to "
    + getName()
       + " with salary " + salary);
    }
    public double getSalary()
     {
       return salary;
     }
    public void setSalary(double newSalary)
    {
       if(newSalary >= 0.0)
       {
          salary = newSalary;
       }
    }
    public double computePay()
    {
      System.out.println("Computing salary
    pay for " + getName());
      return salary/52;
    }
    }