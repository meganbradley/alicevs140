---
title: "Compiler Error CS0053"
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
ms.topic: article
ms.assetid: 62a96ef4-e8d2-44d0-9d39-5cd7a38efe52
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0053
Inconsistent accessibility: property type 'type' is less accessible than property 'property'  
  
 A public construct must return a publicly accessible object. For more information, see [Access Modifiers (C# Programmers Reference)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0053:  
  
```  
// CS0053.cs  
class MyClass //defaults to private accessibility  
// try the following line instead  
// public class MyClass  
{  
}  
  
public class MyClass2  
{  
   public MyClass myProperty   // CS0053  
   {  
      get  
      {  
         return new MyClass();  
      }  
      set  
      {  
      }  
   }  
}  
  
public class MyClass3  
{  
   public static void Main()  
   {  
   }  
}  
```