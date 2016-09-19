---
title: "CMDIFrameWndEx::LoadFrame"
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
ms.assetid: 49d64415-596b-4580-98b2-deec59d77b33
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::LoadFrame
Creates a frame window from resource information.  
  
## Syntax  
  
```  
virtual BOOL LoadFrame(  
   UINT nIDResource,  
   DWORD dwDefaultStyle = WS_OVERLAPPEDWINDOW | FWS_ADDTOTITLE,  
   CWnd* pParentWnd = NULL,  
   CCreateContext* pContext = NULL  
);  
```  
  
#### Parameters  
 [in] `nIDResource`  
 The ID of a shared resource associated with the frame window.  
  
 [in] `dwDefaultStyle`  
 The style of the frame window.  
  
 [in] `pParentWnd`  
 A pointer to the frame's parent.  
  
 [in] `pContext`  
 A pointer to a [CCreateContext Structure](../vs140/CCreateContext-Structure.md). This parameter can be `NULL`.  
  
## Return Value  
 `TRUE` if the method succeeds, otherwise `FALSE`.  
  
## Requirements  
 **Header:** afxmdiframewndex.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)