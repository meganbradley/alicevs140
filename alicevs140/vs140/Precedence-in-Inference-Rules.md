---
title: "Precedence in Inference Rules"
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
ms.assetid: 69e3dc02-0815-4c3a-b02b-1cb85fceaf24
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Precedence in Inference Rules
If an inference rule is multiply defined, NMAKE uses the highest-precedence definition. The following list shows the order of precedence from highest to lowest:  
  
1.  An inference rule defined in a makefile; later definitions have precedence.  
  
2.  An inference rule defined in Tools.ini; later definitions have precedence.  
  
3.  A predefined inference rule.  
  
## See Also  
 [Inference Rules](../vs140/Inference-Rules.md)