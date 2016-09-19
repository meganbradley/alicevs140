---
title: "CMFCVisualManagerOffice2003::OnFillBarBackground"
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
ms.assetid: c9b3c3e9-e6f1-4e14-84e7-6e1079d32519
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnFillBarBackground
The framework calls this method when it fills the background of a [CBasePane](../vs140/CBasePane-Class.md) object.  
  
## Syntax  
  
```  
virtual void OnFillBarBackground(  
   CDC* pDC,  
   CBasePane* pBar,  
   CRect rectClient,  
   CRect rectClip,  
   BOOL bNCArea = FALSE  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to the device context for a control bar.  
  
 [in] `pBar`  
 A pointer to a [CBasePane](../vs140/CBasePane-Class.md) object. The framework fills the background of this pane.  
  
 [in] `rectClient`  
 A rectangle that specifies the boundaries of the pane.  
  
 [in] `rectClip`  
 A rectangle that specifies the clipping area of the pane.  
  
 [in] `bNCArea`  
 A reserved value.  
  
## Remarks  
 The default implementation of this method fills the background of the bar with the 3d background color from the global variable `afxGlobalData`.  
  
 Override this method in a derived visual manager to customize the background of a pane.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)