---
title: "Constant expression is required"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fdd5e7bb-6370-4a63-bbb6-23b15badb4c8
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Constant expression is required
A `Const` statement does not properly initialize a constant, or an array declaration uses a variable to specify the number of elements.  
  
 **Error ID:** BC30059  
  
### To correct this error  
  
1.  If the declaration is a `Const` statement, check to make sure the constant is initialized with a literal, a previously declared constant, an enumeration member, or a combination of literals, constants, and enumeration members combined with operators.  
  
2.  If the declaration specifies an array, check to see if a variable is being used to specify the number of elements. If so, replace the variable with a constant expression.  
  
## See Also  
 [Const Statement](../Topic/Const%20Statement%20\(Visual%20Basic\).md)   
 [NOTINBUILD  an Array Variable](assetId:///c2da78bd-6928-46ba-805f-44f819dfaf93)