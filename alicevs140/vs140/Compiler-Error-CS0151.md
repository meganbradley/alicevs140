---
title: "Compiler Error CS0151"
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
ms.assetid: 1adda08b-6be5-46c8-96f9-5ac7c7bfe48c
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0151
A value of an integral type expected  
  
 A variable was used in a situation where an integral data type was required. For more information, see [Data Types (C# Programmer's Reference)](../Topic/Types%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 This error can occur when there is no conversion or if the available implicit conversions result in an ambiguous situation. The following sample generates CS0151.  
  
```  
// CS0151.cs  
public class MyClass  
{  
   public static implicit operator int (MyClass aa)  
   {  
      return 0;  
   }  
  
   public static implicit operator long (MyClass aa)  
   {  
      return 0;  
   }  
  
   public static void Main()  
   {  
      MyClass a = new MyClass();  
  
      // Compiler cannot choose between int and long  
      switch (a)   // CS0151  
      // try the following line instead  
      // switch ((int)a)  
      {  
         case 1:  
            break;  
      }  
   }  
}  
```  
  
## Example  
 In Visual Studio 2008 and later, a [void](../vs140/void--C#-Reference-.md) method invocation generates CS0151. You can fix the error by calling a method that returns an integral type such as [int](../Topic/int%20\(C%23%20Reference\).md) or [long](../vs140/long--C#-Reference-.md).  
  
```  
class C  
{  
    static void Main()  
    {  
  
        switch (M()) // CS0151  
        {  
            default:  
                break;  
        }  
    }  
  
    static void M()  
    {  
    }  
}  
```