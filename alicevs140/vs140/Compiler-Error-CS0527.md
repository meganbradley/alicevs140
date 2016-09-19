---
title: "Compiler Error CS0527"
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
ms.assetid: 1acd244b-c55b-424f-b038-a130d65b8685
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0527
Type 'type' in interface list is not an interface  
  
 It is possible for a [struct](../vs140/struct--C#-Reference-.md) or [interface](../vs140/interface--C#-Reference-.md) to inherit from another interface but not from any other type.  
  
 The following sample generates CS0527:  
  
```  
// CS0527.cs  
// compile with: /target:library  
public struct clx : int {}   // CS0527 int not an interface  
```