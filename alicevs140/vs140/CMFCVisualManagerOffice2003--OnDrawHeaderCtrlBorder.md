---
title: "CMFCVisualManagerOffice2003::OnDrawHeaderCtrlBorder"
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
ms.assetid: 543112ab-2689-46e7-8341-94a989a2d42b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawHeaderCtrlBorder
The framework calls this method when it draws the border around an instance of the [CMFCHeaderCtrl Class](../vs140/CMFCHeaderCtrl-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawHeaderCtrlBorder(  
   CMFCHeaderCtrl* pCtrl,  
   CDC* pDC,  
   CRect& rect,  
   BOOL bIsPressed,  
   BOOL bIsHighlighted  
);  
```  
  
#### Parameters  
 [in] `pCtrl`  
 A pointer to a [CMFCHeaderCtrl](../vs140/CMFCHeaderCtrl-Class.md) object. The framework draws the border of this header control.  
  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the header control.  
  
 [in] `bIsPressed`  
  [in] `bIsHighlighted`  
 A Boolean parameter that indicates whether the header control is pressed.  
  
## Remarks  
 Override this method in a derived visual manager to customize the border of the header control.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)