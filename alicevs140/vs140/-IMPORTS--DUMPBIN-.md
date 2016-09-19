---
title: "-IMPORTS (DUMPBIN)"
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
H1: /IMPORTS (DUMPBIN)
ms.assetid: 6a296216-2b1b-40f8-8736-cd4553a22456
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -IMPORTS (DUMPBIN)
```  
/IMPORTS[:file]  
```  
  
 This option displays the list of DLLs (both statically linked and [delay loaded](../vs140/Linker-Support-for-Delay-Loaded-DLLs.md)) that are imported to an executable file or DLL and all the individual imports from each of these DLLs.  
  
 The optional `file` specification allows you to specify that the imports for only that DLL will be displayed. For example:  
  
```  
dumpbin /IMPORTS:msvcrt.dll  
```  
  
## Remarks  
 The output displayed by this option is similar to the [/EXPORTS](../vs140/-EXPORTS.md) output.  
  
 Only the [/HEADERS](../vs140/-HEADERS.md) DUMPBIN option is available for use on files produced with the [/GL](../Topic/-GL%20\(Whole%20Program%20Optimization\).md) compiler option.  
  
## See Also  
 [DUMPBIN Options](../vs140/DUMPBIN-Options.md)