---
title: "CPaneFrameWnd::DockPane"
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
ms.assetid: d1e4cd1a-d740-4384-bc77-eb51bc57b742
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::DockPane
Docks the pane.  
  
## Syntax  
  
```  
virtual CDockablePane* DockPane(  
   BOOL& bWasDocked  
);  
```  
  
#### Parameters  
 [out] `bWasDocked`  
 `TRUE` if the pane was already docked; otherwise `FALSE`.  
  
## Return Value  
 If the operation was successful, the `CDockablePane` that the pane was docked to; otherwise `NULL`.  
  
## Requirements  
 **Header:** afxpaneframewnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)