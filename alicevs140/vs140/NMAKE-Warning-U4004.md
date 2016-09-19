---
title: "NMAKE Warning U4004"
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
ms.assetid: 5086bbcb-42d7-4677-a877-1a02202a86a2
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NMAKE Warning U4004
too many rules for target 'targetname'  
  
 More than one description block was specified for the given target using single colons (**:**) as separators. NMAKE executed the commands in the first description block and ignored later blocks.  
  
 To specify the same target in multiple dependencies, use double colons (`::`) as the separator in each dependency line.