---
title: "Fatal Error C1021"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e23171f4-ca6b-40c0-a913-a2edc6fa3766
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1021
invalid preprocessor command 'string'  
  
 `string` is not a valid [preprocessor directive](../vs140/Preprocessor-Directives.md). To resolve the error, use a valid preprocessor name for `string`.  
  
 The following sample generates C1021:  
  
```  
// C1021.cpp  
#BadPreProcName    // C1021 delete line  
```