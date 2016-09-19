---
title: "Compiler Error CS0054"
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
ms.assetid: 49346f55-d887-497a-af71-be4cbbf1de24
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0054
Inconsistent accessibility: indexer return type 'type' is less accessible than indexer 'indexer'  
  
 A public construct must return a publicly accessible object. For more information, see [Access Modifiers (C# Programmer's Reference)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0054:  
  
```  
// CS0054.cs  
class MyClass  
// try the following line instead  
// public class MyClass  
{  
}  
  
public class MyClass3  
{  
   public MyClass this[int i]   // CS0054  
   {  
      get  
      {  
         return new MyClass();  
      }  
   }  
}  
  
public class MyClass2  
{  
   public static void Main()  
   {  
   }  
}  
```