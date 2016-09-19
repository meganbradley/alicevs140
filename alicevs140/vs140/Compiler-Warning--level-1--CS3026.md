---
title: "Compiler Warning (level 1) CS3026"
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
ms.assetid: 6c57b2e3-3011-42db-b450-ce9e04c4b4ca
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS3026
CLS-compliant field 'field' cannot be volatile  
  
 A volatile variable should not be CLS compliant.  
  
## Example  
 The following example generates CS3026.  
  
```  
// CS3026.cs  
[assembly:System.CLSCompliant(true)]  
public class Test  
{  
public volatile int v0 =0;   // CS3026  
      // To resolve remove the CLS-CComplient attribute.  
public static void Main() { }  
}  
  
```