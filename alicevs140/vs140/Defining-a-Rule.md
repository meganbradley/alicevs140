---
title: "Defining a Rule"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 071cd092-3f2e-4065-b0fb-36a9d393cfa8
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Defining a Rule
The *fromext* represents the extension of a dependent file, and *toext* represents the extension of a target file.  
  
```  
.fromext.toext:  
   commands  
```  
  
## Remarks  
 Extensions are not case sensitive. Macros can be invoked to represent *fromext* and *toext*; the macros are expanded during preprocessing. The period (.) preceding *fromext* must appear at the beginning of the line. The colon (:) is preceded by zero or more spaces or tabs. It can be followed only by spaces or tabs, a semicolon (;) to specify a command, a number sign (#) to specify a comment, or a newline character. No other spaces are allowed. Commands are specified as in description blocks.  
  
## What do you want to know more about?  
 [Search paths in rules](../vs140/Search-Paths-in-Rules.md)  
  
## See Also  
 [Inference Rules](../vs140/Inference-Rules.md)