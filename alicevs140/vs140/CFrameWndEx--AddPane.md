---
title: "CFrameWndEx::AddPane"
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
ms.assetid: 9d97d0f5-a953-4267-9ee1-ae4bcdd4c977
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::AddPane
Registers a control bar with the docking manager.  
  
## Syntax  
  
```  
BOOL AddPane(  
   CBasePane* pControlBar,  
   BOOL bTail=TRUE   
);  
```  
  
#### Parameters  
 [in] `pControlBar`  
 A control bar pane to register.  
  
 [in] `bTail`  
 `TRUE` if you want to add the control bar pane to the end of the list; `FALSE` otherwise.  
  
## Return Value  
 `TRUE` if the control bar was successfully registered; `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)