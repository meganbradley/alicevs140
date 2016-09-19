---
title: "CDC::GetBkMode"
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
ms.assetid: 29cfe535-e5b3-40cb-b9b5-32a45f954ce3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetBkMode
Returns the background mode.  
  
## Syntax  
  
```  
  
int GetBkMode( ) const;  
```  
  
## Return Value  
 The current background mode, which can be **OPAQUE** or **TRANSPARENT**.  
  
## Remarks  
 The background mode defines whether the system removes existing background colors on the drawing surface before drawing text, hatched brushes, or any pen style that is not a solid line.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetBkColor](../vs140/CDC--GetBkColor.md)   
 [CDC::SetBkColor](../vs140/CDC--SetBkColor.md)   
 [CDC::SetBkMode](../vs140/CDC--SetBkMode.md)   
 [GetBkMode](http://msdn.microsoft.com/library/windows/desktop/dd144853)