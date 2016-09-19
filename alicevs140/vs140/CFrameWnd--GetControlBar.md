---
title: "CFrameWnd::GetControlBar"
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
ms.assetid: 1d70d22b-8066-4ff2-b364-48692f2fccf7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::GetControlBar
Call `GetControlBar` to gain access to the control bar that is associated with the ID.  
  
## Syntax  
  
```  
  
      CControlBar* GetControlBar(  
   UINT nID   
);  
```  
  
#### Parameters  
 `nID`  
 The ID number of a control bar.  
  
## Return Value  
 A pointer to the control bar that is associated with the ID.  
  
## Remarks  
 The `nID` parameter refers to the unique identifier passed to the **Create** method of the control bar. For more information on control bars, refer to the topic entitled [Control Bars](../vs140/Control-Bars.md).  
  
 `GetControlBar` will return the control bar even if it is floating and thus is not currently a child window of the frame.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)