---
title: "Compiler Warning (level 1) CS1707"
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
ms.assetid: 47b6096e-4e4b-4057-b9d7-4a096139267a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1707
Delegate 'DelegateName' bound to 'MethodName1' instead of 'MethodName2' because of new language rules  
  
 C# 2.0 implements new rules for binding a delegate to a method. Additional information is considered that was not looked at in the past. This warning indicates that the delegate is now bound to a different overload of the method than it was previously bound to. You may wish to verify that the delegate really should be bound to 'MethodName1' instead of 'MethodName2'.  
  
 For a description of how the compiler determines which method to bind a delegate to, see [Covariance and Contravariance in Delegates (C# Programmers Reference)](../vs140/Using-Variance-in-Delegates--C#-and-Visual-Basic-.md).