---
title: "CFrameWndEx::LoadFrame"
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
ms.assetid: 3f8d7a45-25d6-43fe-9bdd-b5eb7a99c245
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::LoadFrame
This method is called after construction to create the frame window and load its resources.  
  
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
 The resource ID that is used to load all frame resources.  
  
 [in] `dwDefaultStyle`  
 The default frame window style.  
  
 [in] `pParentWnd`  
 Pointer to the parent window of the frame.  
  
 [in] `pContext`  
 Pointer to a [CCreateContext](../vs140/CCreateContext-Structure.md) class that is used by the framework during application creation.  
  
## Return Value  
 `TRUE` if the method was successful; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)