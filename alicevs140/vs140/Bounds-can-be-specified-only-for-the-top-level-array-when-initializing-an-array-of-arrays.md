---
title: "Bounds can be specified only for the top-level array when initializing an array of arrays"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d8d7155d-82d1-4a25-b9bb-1883e1586383
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Bounds can be specified only for the top-level array when initializing an array of arrays
An array initialization for a jagged array (array of arrays) sets the initial length of one of the lower levels. You can specify the length of only the top-level array in the array declaration statement.  
  
 **Error ID:** BC32014  
  
### To correct this error  
  
1.  Remove the length specification from all but the top-level array.  
  
2.  Set the initial length of lower-level arrays in subsequent assignment statements using the `New` keyword.  
  
## See Also  
 [NOTINBUILD  an Array Variable](assetId:///c2da78bd-6928-46ba-805f-44f819dfaf93)   
 [NOTINBUILD Jagged Arrays in Visual Basic](assetId:///05c12439-ee8f-4fef-ba75-b35402b67ab9)   
 [New Operator](../vs140/New-Operator--Visual-Basic-.md)