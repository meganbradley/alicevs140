---
title: "Compiler Error CS1019"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 11a3acd8-bcab-4ead-a91b-a1498ea1eab5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1019
Overloadable unary operator expected  
  
 Something that looks like an overloaded unary operator has been declared, but the operator is missing or is in the wrong location in the signature.  
  
 A *unary operator* is an operator that operates on a single operand. For example, `++` is a unary operator. You can overload some unary operators by using the `operator` keyword and specifying a single parameter of the type that the operator operates on. For example, if you want to overload the operator `++` for a user-defined class `Temperature` so that you can write `Temperature++`, you can define it in this way:  
  
```c#  
public static  Temperature operator ++ (Temperature temp)  
{  
    temp.Degrees++;  
    return temp;  
}  
```  
  
 When you receive this error, you have declared something that looks like an overloaded unary operator, except that the operator itself is missing or is in the wrong location in the signature. If you remove the `++` from the signature in the previous example, you will generate CS1019.  
  
 The following code generates CS1019:  
  
```c#  
// CS1019.cs  
public class ii  
{  
   int i  
   {  
      get  
      {  
         return 0;  
      }  
   }  
}  
  
public class a  
{  
    public int i;  
// Generates CS1019: "ii" is not a unary operator.  
   public static a operator ii(a aa)     
  
   // Use the following line instead:  
   //public static a operator ++(a aa)  
   {  
      aa.i++;  
      return aa;   
   }  
  
   public static void Main()  
   {  
   }  
}  
```  
  
## See Also  
 [Operators (C# Programming Guide)](../Topic/Operators%20\(C%23%20Programming%20Guide\).md)