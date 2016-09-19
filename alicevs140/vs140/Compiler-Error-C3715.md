---
title: "Compiler Error C3715"
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
ms.assetid: ee5dce88-ddc4-4bdb-9464-47467ce1674f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3715
'pointer': must be a pointer to 'class'  
  
 You specified a pointer in [__hook](../vs140/__hook.md) or [__unhook](../vs140/__unhook.md) that did not point to a valid class. To fix this error, ensure that your `__hook` and `__unhook` calls specify pointers to valid classes.