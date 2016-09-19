---
title: "CPathT::CompactPath"
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
ms.assetid: c06b9abd-9122-42c5-b118-d2b40dff5af0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::CompactPath
Call this method to truncate a file path to fit within a given pixel width by replacing path components with ellipses.  
  
## Syntax  
  
```  
  
      BOOL CompactPath(  
   HDC hDC,  
   UINT nWidth   
);  
```  
  
#### Parameters  
 `hDC`  
 The device context used for font metrics.  
  
 `nWidth`  
 The width, in pixels, that the string will be forced to fit in.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Remarks  
 For more information, see [PathCompactPath](http://msdn.microsoft.com/library/windows/desktop/bb773575).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)   
 [CPathT::CompactPathEx](../vs140/CPathT--CompactPathEx.md)