---
title: "CBasePane::CanBeDocked"
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
ms.assetid: e1cde857-9c55-41ce-bc17-ff314dcb70c4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::CanBeDocked
Determines whether the pane can be docked to another pane.  
  
## Syntax  
  
```  
virtual BOOL CanBeDocked(  
   CBasePane* pDockBar    
) const;  
```  
  
#### Parameters  
 [in] `pDockBar`  
 A pointer to another pane.  
  
## Return Value  
 `TRUE` if this pane can be docked to another pane; otherwise `FALSE`.  
  
## Remarks  
 The framework calls this method before it docks the pane specified by `pDockBar` to the current pane.  
  
 Use this method and the  [CBasePane::CanAcceptPane](../vs140/CBasePane--CanAcceptPane.md) method to control how panes dock to other panes in your application.  
  
 The default implementation returns `FALSE`.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)