---
title: "CMFCVisualManager::OnDrawHeaderCtrlBorder"
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
ms.assetid: a1cb9a6c-1ae5-4b24-9a14-09d7fdaa8ed1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawHeaderCtrlBorder
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
 A pointer to a `CMFCHeaderCtrl` object. The framework draws the border of this header control.  
  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the header control.  
  
 [in] `bIsPressed`  
 A Boolean parameter that indicates whether the header control is pressed.  
  
 [in] `bIsHighlighted`  
 A Boolean parameter that indicates whether the header control is highlighted.  
  
## Remarks  
 Override this method in a derived visual manager to customize the border of the header control.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCHeaderCtrl Class](../vs140/CMFCHeaderCtrl-Class.md)