---
title: "Compiler Error CS0529"
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
ms.assetid: 61de8086-f991-455c-b009-bb8cd05f34bd
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0529
Inherited interface 'interface1' causes a cycle in the interface hierarchy of 'interface2'  
  
 The inheritance list for an [interface](../vs140/interface--C#-Reference-.md) includes a direct or indirect reference to itself. An interface cannot inherit from itself.  
  
 The following sample generates CS0529:  
  
```  
// CS0529.cs  
namespace x  
{  
   public interface a  
   {  
   }  
  
   public interface b : a, c  
   {  
   }  
  
   public interface c : b   // CS0529, b inherits from c  
   {  
   }  
}  
```