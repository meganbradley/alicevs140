---
title: "LIB Output Files"
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
ms.assetid: e73d2f9b-a42d-402b-b7e3-3a94bebb317e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LIB Output Files
The output files produced by LIB depend on the mode in which it is being used, as shown in the following table.  
  
|Mode|Output|  
|----------|------------|  
|Default (building or modifying a library)|COFF library (.lib)|  
|Extracting a member with /EXTRACT|Object (.obj) file|  
|Building an export file and import library with /DEF|Import library (.lib) and export (.exp) file|  
  
## See Also  
 [Overview of LIB](../vs140/Overview-of-LIB.md)