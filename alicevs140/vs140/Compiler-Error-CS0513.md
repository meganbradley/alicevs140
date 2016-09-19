---
title: "Compiler Error CS0513"
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
ms.topic: article
ms.assetid: 6f8569df-713d-4c9c-a675-6576dad139ce
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0513
'function' is abstract but it is contained in nonabstract class 'class'  
  
 A method cannot be an [abstract](../vs140/abstract--C#-Reference-.md) member of a nonabstract class.  
  
 The following sample generates CS0513:  
  
```  
// CS0513.cs  
namespace x  
{  
   public class clx  
   {  
      abstract public void f();   // CS0513, abstract member of nonabstract class  
   }  
}  
```