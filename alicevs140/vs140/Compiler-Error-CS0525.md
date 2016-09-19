---
title: "Compiler Error CS0525"
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
ms.assetid: fcecfd4f-221f-41e6-a95c-1685be78926e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0525
Interfaces cannot contain fields  
  
 An [interface](../vs140/interface--C#-Reference-.md) can contain methods and properties but not fields.  
  
 The following sample generates CS0525:  
  
```  
// CS0525.cs  
namespace x  
{  
   public interface clx  
   {  
      public int i;   // CS0525  
   }  
}  
```