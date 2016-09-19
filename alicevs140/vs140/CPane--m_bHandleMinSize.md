---
title: "CPane::m_bHandleMinSize"
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
ms.assetid: bde2091b-79b8-4b89-990f-b6a8bd63e484
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::m_bHandleMinSize
Enables consistent handling of minimum pane sizes.  
  
## Syntax  
  
```  
AFX_IMPORT_DATA static BOOL m_bHandleMinSize;  
```  
  
## Remarks  
 If one or more docking panes in your application override `GetMinSize`, or if your application calls `SetMinSize`, you may want to set this static member to `TRUE` in order to enable the framework to consistently handle how panes are sized.  
  
 If this value is set to `TRUE`, all panes whose size should be reduced below their minimum size are clipped, not stretched. Because the framework uses window regions for pane sizing purposes, do not change the size of the window region for docking panes if this value is set to `TRUE`.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)