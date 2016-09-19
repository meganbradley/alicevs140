---
title: "CMFCToolBarDateTimeCtrl::OnChangeParentWnd"
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
ms.assetid: 5aba4e6f-68ee-455b-b278-966da385be76
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::OnChangeParentWnd
Called by the framework when the button is inserted into a new toolbar.  
  
## Syntax  
  
```  
virtual void OnChangeParentWnd(  
   CWnd* pWndParent  
);  
```  
  
#### Parameters  
 [in] `pWndParent`  
 The new parent window.  
  
## Remarks  
 This method overrides the base class implementation ([CMFCToolBarButton::OnChangeParentWnd](../vs140/CMFCToolBarButton--OnChangeParentWnd.md)) by recreating the internal `CMFCToolBarDateTimeCtrlImpl` object.  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnChangeParentWnd](../vs140/CMFCToolBarButton--OnChangeParentWnd.md)   
 [CMFCToolBarDateTimeCtrlImpl Class](assetId:///4fcddcbc-b374-4c27-bfb4-09fb0ca2eac5)