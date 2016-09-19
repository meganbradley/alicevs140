---
title: "Running NMAKE"
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
ms.assetid: 0421104d-8b7b-4bf3-86c1-928d9b7c1a8c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Running NMAKE
## Syntax  
  
```  
NMAKE [option...] [macros...] [targets...] [@commandfile...]  
```  
  
## Remarks  
 NMAKE builds only specified *targets* or, if none is specified, the first target in the makefile. The first makefile target can be a [pseudotarget](../vs140/Pseudotargets.md) that builds other targets. NMAKE uses makefiles specified with /F; if /F is not specified, it uses the Makefile file in the current directory. If no makefile is specified, it uses inference rules to build command-line *targets*.  
  
 The `commandfile` text file (or response file) contains command-line input. Other input can precede or follow @`commandfile`. A path is permitted. In `commandfile`, line breaks are treated as spaces. Enclose macro definitions in quotation marks if they contain spaces.  
  
## What do you want to know more about?  
 [NMAKE options](../vs140/NMAKE-Options.md)  
  
 [Tools.ini and NMAKE](../vs140/Tools.ini-and-NMAKE.md)  
  
 [Exit codes from NMAKE](../vs140/Exit-Codes-from-NMAKE.md)  
  
## See Also  
 [NMAKE Reference](../vs140/NMAKE-Reference.md)