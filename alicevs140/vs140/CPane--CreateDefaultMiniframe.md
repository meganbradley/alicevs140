---
title: "CPane::CreateDefaultMiniframe"
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
ms.assetid: d8a4c1f9-ef6c-4b0f-898e-8421c2721d90
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::CreateDefaultMiniframe
Creates a mini-frame window for a floating pane.  
  
## Syntax  
  
```  
virtual CPaneFrameWnd* CreateDefaultMiniframe(  
    CRect rectInitial  
);  
```  
  
#### Parameters  
 [in] `rectInitial`  
 Specifies the initial size and position, in screen coordinates, of the mini-frame window to create.  
  
## Return Value  
 The newly created mini-frame window.  
  
## Remarks  
 This method is called by the framework to create a mini-frame window when a pane is floated. The mini-frame window can be of type [CPaneFrameWnd](../vs140/CPaneFrameWnd-Class.md) or of type [CMultiPaneFrameWnd](../vs140/CMultiPaneFrameWnd-Class.md). A multi mini-frame window is created if the pane has the `AFX_CBRS_FLOAT_MULTI` style.  
  
 The runtime class information for the mini-frame window is stored in the `CPane::m_pMiniFrameRTC` member. You can use a derived class to set this member if you decide to create customized mini-frame windows.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)