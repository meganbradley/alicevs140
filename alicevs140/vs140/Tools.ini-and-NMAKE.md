---
title: "Tools.ini and NMAKE"
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
ms.assetid: ebd5eab6-ddf4-430e-bf4a-1db5bb84e344
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Tools.ini and NMAKE
NMAKE reads Tools.ini before it reads makefiles, unless /R is used. It looks for Tools.ini first in the current directory and then in the directory specified by the INIT environment variable. The section for NMAKE settings in the initialization file begins with `[NMAKE]` and can contain any makefile information. Specify a comment on a separate line beginning with a number sign (#).  
  
## See Also  
 [Running NMAKE](../vs140/Running-NMAKE.md)