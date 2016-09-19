---
title: "CMFCVisualManagerOffice2003::OnDrawStatusBarSizeBox"
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
ms.assetid: 78a8a978-946f-4ac9-8970-517dc12d54e9
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawStatusBarSizeBox
The framework calls this method when it draws the size box for a [CMFCStatusBar](../vs140/CMFCStatusBar-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawStatusBarSizeBox(  
   CDC* pDC,  
   CMFCStatusBar* pStatBar,  
   CRect rectSizeBox  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pStatBar`  
 A pointer to a status bar. The framework draws the size box for this status bar.  
  
 [in] `rectSizeBox`  
 A rectangle that specifies the boundaries of the size box.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of the size box on a status bar.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)