---
title: "CPane::CalcInsideRect"
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
ms.assetid: b9fd483b-378c-48e3-9098-cec007105c9a
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::CalcInsideRect
Calculates the inside rectangle of a pane, including the borders and grippers.  
  
## Syntax  
  
```  
void CalcInsideRect(  
    CRect& rect,  
    BOOL bHorz   
) const;  
```  
  
#### Parameters  
 [out] `rect`  
 Contains the size and offset of the client area of the pane.  
  
 [in] `bHorz`  
 `TRUE` if the pane is oriented horizontally; otherwise, `FALSE`.  
  
## Remarks  
 This method is called by the framework when it has to recalculate the layout for a pane. The `rect` parameter is filled with the size and offset of the client area of the pane. This includes its borders and grippers.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)