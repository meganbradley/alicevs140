---
title: "Compiler Warning (level 4) C4235"
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
ms.assetid: d4214799-d62c-4674-b4e2-9e201c303303
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4235
nonstandard extension used : 'keyword' keyword not supported on this architecture  
  
 The compiler does not support the keyword you used.  
  
 This warning is automatically promoted to an error. If you wish to modify this behavior, use [#pragma warning](../vs140/warning.md). For example, to make C4235 into a level 2 warning, use the following line of code  
  
```  
#pragma warning(2:4235)  
```  
  
 in your source code file.