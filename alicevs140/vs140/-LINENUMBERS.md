---
title: "-LINENUMBERS"
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
H1: /LINENUMBERS
ms.assetid: 1681d582-2c2f-484e-9920-109959549055
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -LINENUMBERS
```  
/LINENUMBERS  
```  
  
## Remarks  
 This option displays COFF line numbers. Line numbers exist in an object file if it was compiled with Program Database (/Zi), C7 Compatible (/Z7), or Line Numbers Only (/Zd). An executable file or DLL contains COFF line numbers if it was linked with Generate Debug Info (/DEBUG).  
  
 Only the [/HEADERS](../vs140/-HEADERS.md) DUMPBIN option is available for use on files produced with the [/GL](../Topic/-GL%20\(Whole%20Program%20Optimization\).md) compiler option.  
  
## See Also  
 [DUMPBIN Options](../vs140/DUMPBIN-Options.md)