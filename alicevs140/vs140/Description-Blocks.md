---
title: "Description Blocks"
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
ms.assetid: 1321f228-d389-40ac-b0cd-4f6e9293602b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Description Blocks
A description block is a dependency line optionally followed by a commands block:  
  
```  
targets... : dependents...  
    commands...  
```  
  
 A dependency line specifies one or more targets and zero or more dependents. A target must be at the start of the line. Separate targets from dependents by a colon (:); spaces or tabs are allowed. To split the line, use a backslash (\ ) after a target or dependent. If a target does not exist, has an earlier timestamp than a dependent, or is a [pseudotarget](../vs140/Pseudotargets.md), NMAKE executes the commands. If a dependent is a target elsewhere and does not exist or is out-of-date with respect to its own dependents, NMAKE updates the dependent before updating the current dependency.  
  
## What do you want to know more about?  
 [Targets](../vs140/Targets.md)  
  
 [Dependents](../vs140/Dependents.md)  
  
## See Also  
 [NMAKE Reference](../vs140/NMAKE-Reference.md)