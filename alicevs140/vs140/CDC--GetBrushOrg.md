---
title: "CDC::GetBrushOrg"
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
ms.assetid: 7aa9dd42-f6b7-405a-b99c-79e148dcc0ed
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetBrushOrg
Retrieves the origin (in device units) of the brush currently selected for the device context.  
  
## Syntax  
  
```  
  
CPoint GetBrushOrg( ) const;  
```  
  
## Return Value  
 The current origin of the brush (in device units) as a [CPoint](../vs140/CPoint-Class.md) object.  
  
## Remarks  
 The initial brush origin is at (0,0) of the client area. The return value specifies this point in device units relative to the origin of the desktop window.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetBrushOrg](../vs140/CDC--SetBrushOrg.md)   
 [CPoint Class](../vs140/CPoint-Class.md)