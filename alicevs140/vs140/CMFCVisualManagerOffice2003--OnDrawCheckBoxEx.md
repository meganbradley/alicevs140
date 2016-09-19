---
title: "CMFCVisualManagerOffice2003::OnDrawCheckBoxEx"
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
ms.assetid: 20524316-1a07-47f6-af69-2ae4f5ffb30b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawCheckBoxEx
Called by the framework when drawing a checkbox.  
  
## Syntax  
  
```  
virtual void OnDrawCheckBoxEx(  
   CDC *pDC,  
   CRect rect,  
   int nState,  
   BOOL bHighlighted,  
   BOOL bPressed,  
   BOOL bEnabled  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a device context.  
  
 [in] `rect`  
 The bounding rectangle of the checkbox.  
  
 [in] `nState`  
 The state of the checkbox: 0 if unchecked, 1 if checked, 2 if checked mixed.  
  
 [in] `bHighlighted`  
 `TRUE` if the checkbox is highlighted, or `FALSE` if not.  
  
 [in] `bPressed`  
 `TRUE` if the checkbox is pressed, or `FALSE` if not.  
  
 [in] `bEnabled`  
 `TRUE` if the checkbox is enabled, or `FALSE` if not.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)