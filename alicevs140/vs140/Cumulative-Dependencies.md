---
title: "Cumulative Dependencies"
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
ms.assetid: fa6dd777-80b8-437d-87a7-aec0ed818a49
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Cumulative Dependencies
Dependencies are cumulative in a description block if a target is repeated.  
  
 For example, this set of rules,  
  
 **bounce.exe : jump.obj**  
**bounce.exe : up.obj**  
 **echo Building bounce.exe...** is evaluated as this:  
  
 **bounce.exe : jump.obj up.obj**  
 **echo Building bounce.exe...** Multiple targets in multiple dependency lines in a single description block are evaluated as if each were specified in a separate description block, but targets that are not in the last dependency line do not use the commands block. NMAKE attempts to use an inference rule for such targets.  
  
 For example, this set of rules,  
  
 **leap.exe bounce.exe : jump.obj**  
**bounce.exe climb.exe : up.obj**  
 **echo Building bounce.exe...** is evaluated as this:  
  
  **leap.exe : jump.obj**  
**# invokes an inference rule**  
**bounce.exe : jump.obj up.obj**  
 **echo Building bounce.exe...**  
**climb.exe : up.obj**  
 **echo Building bounce.exe...**   
## See Also  
 [Targets](../vs140/Targets.md)