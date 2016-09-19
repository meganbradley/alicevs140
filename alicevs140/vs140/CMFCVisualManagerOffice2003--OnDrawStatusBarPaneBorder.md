---
title: "CMFCVisualManagerOffice2003::OnDrawStatusBarPaneBorder"
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
ms.assetid: a06ec8f7-1583-40ed-b32b-b4e1a16d6df3
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawStatusBarPaneBorder
The framework calls this method when it draws the border for a [CMFCStatusBar](../vs140/CMFCStatusBar-Class.md) object.  
  
## Syntax  
  
```  
virtual void OnDrawStatusBarPaneBorder(  
   CDC* pDC,  
   CMFCStatusBar* pBar,  
   CRect rectPane,  
   UINT uiID,  
   UINT nStyle  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pBar`  
 A pointer to a [CMFCStatusBar](../vs140/CMFCStatusBar-Class.md) object. The framework draws this status bar object.  
  
 [in] `rectPane`  
 A rectangle that specifies the boundaries of the status bar.  
  
 [in] `uiID`  
 The ID of the status bar.  
  
 [in] `nStyle`  
 The style of the status bar.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of the border for a `CMFCStatusBar` object.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)