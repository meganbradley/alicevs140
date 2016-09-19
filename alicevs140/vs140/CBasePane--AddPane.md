---
title: "CBasePane::AddPane"
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
ms.assetid: 8c5844dd-895f-404e-82e7-ae32e7a660d1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::AddPane
Adds a pane to the docking manager.  
  
## Syntax  
  
```  
void AddPane(  
   CBasePane* pBar  
);  
```  
  
#### Parameters  
 [in] `pBar`  
 A pointer to a pane to add.  
  
## Remarks  
 This is a convenience method that adds a pane to a docking manager. By using this method, you do not have to write code that analyzes the type of the parent frame.  
  
 For more information, see [CDockingManager Class](../vs140/CDockingManager-Class.md) and [CMDIFrameWndEx::AddPane](../vs140/CMDIFrameWndEx--AddPane.md).  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)