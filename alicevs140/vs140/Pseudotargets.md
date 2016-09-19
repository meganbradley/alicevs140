---
title: "Pseudotargets"
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
ms.assetid: c8c479dc-0129-4186-8366-bc6251f2b494
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Pseudotargets
A pseudotarget is a label used in place of a filename in a dependency line. It is interpreted as a file that does not exist, and so is out-of-date. NMAKE assumes a pseudotarget's timestamp is the most recent of all its dependents. If it has no dependents, the current time is assumed. If a pseudotarget is used as a target, its commands are always executed. A pseudotarget used as a dependent must also appear as a target in another dependency. However, that dependency does not need to have a commands block.  
  
 Pseudotarget names follow the filename syntax rules for targets. However, if the name does not have an extension (that is, does not contain a period), it can exceed the 8-character limit for filenames and can be up to 256 characters long.  
  
## See Also  
 [Targets](../vs140/Targets.md)