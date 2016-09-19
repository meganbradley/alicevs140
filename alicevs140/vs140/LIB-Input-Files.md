---
title: "LIB Input Files"
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
ms.assetid: e1236f0d-cd90-446b-b900-f311f456085c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LIB Input Files
The input files expected by LIB depend on the mode in which it is being used, as shown in the following table.  
  
|Mode|Input|  
|----------|-----------|  
|Default (building or modifying a library)|COFF object (.obj) files, COFF libraries (.lib), 32-bit Object Model Format (OMF) object (.obj) files|  
|Extracting a member with /EXTRACT|COFF library (.lib)|  
|Building an export file and import library with /DEF|Module-definition (.def) file, COFF object (.obj) files, COFF libraries (.lib), 32-bit OMF object (.obj) files|  
  
> [!NOTE]
>  OMF libraries created by the 16-bit version of LIB cannot be used as input to the 32-bit version of LIB.  
  
## See Also  
 [Overview of LIB](../vs140/Overview-of-LIB.md)