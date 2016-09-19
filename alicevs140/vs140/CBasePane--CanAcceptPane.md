---
title: "CBasePane::CanAcceptPane"
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
ms.assetid: fc49e62c-de9f-4f1c-8d50-5cb30acbe341
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::CanAcceptPane
Determines whether another pane can be docked to the pane.  
  
## Syntax  
  
```  
virtual BOOL CanAcceptPane(  
   const CBasePane* pBar   
) const;  
```  
  
#### Parameters  
 [in] `pBar`  
 A pointer to the pane to dock.  
  
## Return Value  
 `TRUE` if another pane can be accepted; otherwise `FALSE`.  
  
## Remarks  
 The framework calls this method before it docks the pane specified by `pBar` to the current pane.  
  
 Use this method and the [CanBeDocked](../vs140/CBasePane--CanBeDocked.md) method to control how panes dock to other panes in your application.  
  
 The default implementation returns `FALSE`.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)