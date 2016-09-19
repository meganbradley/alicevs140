---
title: "Compiler Error CS1540"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: f35bbeb9-e2b2-4644-a7e6-cc2dbce1bd44
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1540
Cannot access protected member 'member' via a qualifier of type 'type1'; the qualifier must be of type 'type2' (or derived from it)  
  
 A derived [class](../vs140/class--C#-Reference-.md) cannot access protected members of its base class through an instance of the base class. An instance of the base class declared in the derived class might, at run time, be an instance of another type that is derived from the same base but is not otherwise related to the derived class. Because protected members can be accessed only by derived types, any attempts to access protected members that might not be valid at run time are marked by the compiler as not valid.  
  
 In the `Employee` class in the following example, `emp2` and `emp3` both have type `Person` at compile time, but `emp2` has type `Manager` at run time. Because `Employee` is not derived from `Manager`, it cannot access the protected members of the base class, `Person`, through an instance of the `Manager` class. The compiler cannot determine what the run-time type of the two `Person` objects will be. Therefore, both the call from `emp2` and the call from `emp3` cause compiler error CS1540.  
  
```c#  
using System;  
using System.Text;  
  
namespace CS1540  
{  
    class Program1  
    {  
        static void Main()  
        {  
            Employee.PreparePayroll();  
        }  
    }  
  
    class Person  
    {  
        protected virtual void CalculatePay()   
        {  
            Console.WriteLine("CalculatePay in Person class.");  
        }  
    }  
  
    class Manager : Person  
    {  
        protected override void CalculatePay()   
        {  
            Console.WriteLine("CalculatePay in Manager class.");   
  
        }  
    }  
  
    class Employee : Person  
    {  
        public static void PreparePayroll()  
        {  
            Employee emp1 = new Employee();  
            Person emp2 = new Manager();  
            Person emp3 = new Employee();  
            // The following line calls the method in the Employee base class,  
            // Person.  
            emp1.CalculatePay();   
  
            // The following lines cause compiler error CS1540. The compiler   
            // cannot determine at compile time what the run-time types of   
            // emp2 and emp3 will be.  
            //emp2.CalculatePay();   
            //emp3.CalculatePay();  
  
        }  
    }  
}  
```  
  
## See Also  
 [Inheritance (C# Programming Guide)](../Topic/Inheritance%20\(C%23%20Programming%20Guide\).md)   
 [Polymorphism (C# Programming Guide)](../Topic/Polymorphism%20\(C%23%20Programming%20Guide\).md)   
 [Access Modifiers (C# Programming Guide)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)   
 [Abstract and Sealed Classes and Class Members (C# Programming Guide)](../vs140/Abstract-and-Sealed-Classes-and-Class-Members--C#-Programming-Guide-.md)