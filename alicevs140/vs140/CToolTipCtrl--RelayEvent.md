---
title: "CToolTipCtrl::RelayEvent"
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
ms.assetid: 145b1413-1606-4f57-8c76-bee539a6f264
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::RelayEvent
Passes a mouse message to a tool tip control for processing.  
  
## Syntax  
  
```  
  
      void RelayEvent(  
   LPMSG lpMsg   
);  
```  
  
#### Parameters  
 `lpMsg`  
 Pointer to a [MSG](http://msdn.microsoft.com/library/windows/desktop/ms644958) structure that contains the message to relay.  
  
## Remarks  
 A tool tip control processes only the following messages, which are sent to it by `RelayEvent`:  
  
|WM_LBUTTONDOWN|WM_MOUSEMOVE|  
|---------------------|-------------------|  
|`WM_LBUTTONUP`|`WM_RBUTTONDOWN`|  
|`WM_MBUTTONDOWN`|`WM_RBUTTONUP`|  
|`WM_MBUTTONUP`||  
  
## Example  
 See the example for [CPropertySheet::GetTabControl](../vs140/CPropertySheet--GetTabControl.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::PreTranslateMessage](../vs140/CWnd--PreTranslateMessage.md)   
 [CWinApp::PreTranslateMessage](../vs140/CWinApp--PreTranslateMessage.md)