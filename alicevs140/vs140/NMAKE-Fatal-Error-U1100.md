---
title: "NMAKE Fatal Error U1100"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: c71910a7-c581-4d9c-a38c-d2d557d56289
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NMAKE Fatal Error U1100
macro 'macroname' is illegal in the context of batch rule 'rule'  
  
 NMAKE generates this error when the command block of a batch-mode rule directly or indirectly references a special file macro that is not $<.  
  
 $< is the only allowed macro for batch-mode rules.