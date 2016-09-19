---
title: "CPathT::FindFileName"
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
ms.assetid: 820540bc-dcfb-406e-86c1-10248b621348
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::FindFileName
Call this method to find the position of the file name within the path.  
  
## Syntax  
  
```  
  
int FindFileName( ) const;  
  
```  
  
## Return Value  
 Returns the position of the file name. If no file name is found, returns –1.  
  
## Remarks  
 For more information, see [PathFindFileName](http://msdn.microsoft.com/library/windows/desktop/bb773589).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)