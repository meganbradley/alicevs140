---
title: "CPathT::StripToRoot"
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
ms.topic: reference
ms.assetid: 4d832373-1845-49ec-a990-259af6e99506
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::StripToRoot
Call this method to remove all parts of the path except for the root information.  
  
## Syntax  
  
```  
  
BOOL StripToRoot( );  
  
```  
  
## Return Value  
 Returns TRUE if a valid drive letter was found in the path, or FALSE otherwise.  
  
## Remarks  
 For more information, see [PathStripToRoot](http://msdn.microsoft.com/library/windows/desktop/bb773757).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)