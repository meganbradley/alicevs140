---
title: "Compiler Warning (level 3) C4723"
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
ms.assetid: 07669d14-3fd8-4a43-94bc-b61c50e58460
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4723
potential divide by 0  
  
 The second operand in a divide operation evaluated to zero at compile time, giving undefined results.  
  
 This warning is issued only when using [/Og](../vs140/-Og--Global-Optimizations-.md) or an optimization option that implies /Og.  
  
 The compiler may have generated the zero operand.