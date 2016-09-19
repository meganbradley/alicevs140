---
title: "Compiler Error CS0571"
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
ms.assetid: 72a97e9c-3c78-47de-b477-dbd2c953d95d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0571
'function' : cannot explicitly call operator or accessor  
  
 Certain operators have internal names. For example, **op_Increment** is the internal name of the ++ operator. You should not use or explicitly call such method names.  
  
 The following sample generates CS0571:  
  
```  
// CS0571.cs  
public class MyClass  
{  
   public static MyClass operator ++ (MyClass c)  
   {  
      return null;  
   }  
  
   public static int prop  
   {  
      get  
      {  
         return 1;  
      }  
      set  
      {  
      }  
   }  
  
   public static void Main()  
   {  
      op_Increment(null);   // CS0571  
      // use the increment operator as follows  
      // MyClass x = new MyClass();  
      // x++;  
  
      set_prop(1);      // CS0571  
      // try the following line instead  
      // prop = 1;  
   }  
}  
```