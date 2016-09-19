---
title: "Compiler Warning (level 1) C4083"
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
ms.topic: error-reference
ms.assetid: e7d3344e-5645-4d56-8460-d1acc9145ada
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4083
expected 'token'; found identifier 'identifier'  
  
 An identifier occurs in the wrong place in a **#pragma** statement.  
  
## Example  
  
```  
// C4083.cpp  
// compile with: /W1 /LD  
#pragma warning disable:4083    // C4083  
#pragma warning(disable:4083)   //correct  
```  
  
 Check the syntax of the [#pragma](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md) directives.