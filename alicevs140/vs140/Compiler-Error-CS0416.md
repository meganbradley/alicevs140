---
title: "Compiler Error CS0416"
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
ms.assetid: 61bfe40d-5e87-47e5-933f-3491e28ace42
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0416
'type parameter': an attribute argument cannot use type parameters  
  
 A type parameter was used as an attribute argument, which is not allowed. Use a non-generic type.  
  
 The following sample generates CS0416:  
  
```  
// CS0416.cs  
public class MyAttribute : System.Attribute  
{  
   public MyAttribute(System.Type t)  
   {  
   }  
}  
  
class G<T>  
{  
  
   [MyAttribute(typeof(G<T>))]  // CS0416  
   public void F()  
   {  
   }  
  
}  
```