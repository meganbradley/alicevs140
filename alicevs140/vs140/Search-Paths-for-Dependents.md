---
title: "Search Paths for Dependents"
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
ms.assetid: bf998e47-da74-48b5-891d-d3d8ce57264b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Search Paths for Dependents
Each dependent has an optional search path, specified as follows:  
  
## Syntax  
  
```  
{directory[;directory...]}dependent  
```  
  
## Remarks  
 NMAKE looks for a dependent first in the current directory, and then in directories in the order specified. A macro can specify part or all of a search path. Enclose directory names in braces ({ }); separate multiple directories with a semicolon (;). No spaces or tabs are allowed.  
  
## See Also  
 [Dependents](../vs140/Dependents.md)