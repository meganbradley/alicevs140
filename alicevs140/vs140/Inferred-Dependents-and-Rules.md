---
title: "Inferred Dependents and Rules"
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
ms.assetid: 9381e74a-53d9-445c-836d-0ff7ef6112d9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Inferred Dependents and Rules
NMAKE assumes an inferred dependent for a target if an applicable inference rule exists. A rule applies if:  
  
-   *toext* matches the target's extension.  
  
-   *fromext* matches the extension of a file that has the target's base name and that exists in the current or specified directory.  
  
-   *fromext* is in [.SUFFIXES](../vs140/Dot-Directives.md); no other *fromext* in a matching rule has a higher **.SUFFIXES** priority.  
  
-   No explicit dependent has a higher **.SUFFIXES** priority.  
  
 Inferred dependents can cause unexpected side effects. If the target's description block contains commands, NMAKE executes those commands instead of the commands in the rule.  
  
## See Also  
 [Inference Rules](../vs140/Inference-Rules.md)