---
title: "Compiler Warning (level 1) C4076"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 04581066-313a-4a11-bb60-721e6d038d75
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4076
'typemod' : can not be used with type 'typename'  
  
 A type modifier, whether it is **signed** or `unsigned`, cannot be used with a noninteger type. ***typemod*** is ignored.  
  
## Example  
 The following sample generates C4076:  
  
```  
// C4076.cpp  
// compile with: /W1 /LD  
unsigned double x;   // C4076  
```