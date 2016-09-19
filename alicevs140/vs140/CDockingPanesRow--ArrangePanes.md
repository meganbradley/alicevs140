---
title: "CDockingPanesRow::ArrangePanes"
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
ms.assetid: 645c0ebb-0ef4-40b3-a492-96f5b904ec1e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingPanesRow::ArrangePanes
Arranges docking panes in a row according to the specified margin and spacing parameters.  
  
## Syntax  
  
```  
virtual void ArrangePanes(  
    int nMargin,  
    int nSpacing   
);  
```  
  
#### Parameters  
 [in] `nMargin`  
 Specifies the offset, in pixels, of the first pane from the upper-left corner of the row.  
  
 [in] `nSpacing`  
 Specifies the spacing, in pixels, between panes.  
  
## Remarks  
 Call this method to arrange panes in the row where they will dock. After calling this method, you must call `CDockingPanesRow::FixupVirtualRects(FALSE, NULL)`.  
  
## Requirements  
 **Header:** afxDockingPanesRow.h  
  
## See Also  
 [CDockingPanesRow Class](../vs140/CDockingPanesRow-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)