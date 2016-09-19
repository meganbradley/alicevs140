---
title: "Compiler Warning (level 4) C4234"
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
ms.assetid: f7fecd5c-8248-4fde-8446-502aedc357ca
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4234
nonstandard extension used: 'keyword' keyword reserved for future use  
  
 The compiler does not yet implement the keyword you used.  
  
 This warning is automatically promoted to an error. If you wish to modify this behavior, use [#pragma warning](../vs140/warning.md). For example, to make C4234 into a level 4 warning issue,  
  
```  
#pragma warning(2:4234)  
```  
  
 in your source code file.