---
title: "Compiler Error CS0120"
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
ms.assetid: 3ff67f11-bdf9-436b-bc0c-4fa3cd1925a6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0120
An object reference is required for the nonstatic field, method, or property 'member'  
  
 In order to use a non-static field, method, or property, you must first create an object instance. For more information about static methods, see [Static Classes and Static Class Members (C# Programming Guide)](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md). For more information about creating instances of classes, see [Instance Constructors (C# Programmer's Reference)](../vs140/Instance-Constructors--C#-Programming-Guide-.md).  
  
 The following sample generates CS0120:  
  
```  
// CS0120_1.cs  
public class MyClass  
{  
   // Non-static field  
   public int i;   
   // Non-static method  
   public void f(){}  
   // Non-static property  
   int Prop  
   {  
      get   
      {  
         return 1;   
      }  
   }  
  
   public static void Main()  
   {  
      i = 10;   // CS0120  
      f();   // CS0120  
      int p = Prop;   // CS0120  
      // try the following lines instead  
      // MyClass mc = new MyClass();  
      // mc.i = 10;  
      // mc.f();  
      // int p = mc.Prop;  
   }  
}  
```  
  
 CS0120 will also be generated if there is a call to a non-static method from a static method, as follows:  
  
```  
// CS0120_2.cs  
// CS0120 expected  
using System;  
  
public class MyClass  
{  
   public static void Main()  
   {  
      TestCall();   // CS0120  
      // To call a non-static method from Main,  
      // first create an instance of the class.  
      // Use the following two lines instead:  
      // MyClass anInstanceofMyClass = new MyClass();  
      // anInstanceofMyClass.TestCall();  
   }  
  
   public void TestCall()  
   {  
   }  
}  
```  
  
 Similarly, a static method cannot call an instance method unless you explicitly give it an instance of the class, as follows:  
  
```  
// CS0120_3.cs  
using System;  
  
public class MyClass  
{  
   public static void Main()  
   {  
      do_it("Hello There");   // CS0120  
   }  
  
   private void do_it(string sText)  
   // You could also add the keyword static to the method definition:  
   // private static void do_it(string sText)  
   {  
      Console.WriteLine(sText);  
   }  
}  
```  
  
## See Also  
 [Objects, Classes and Structs (C# Programming Guide)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)