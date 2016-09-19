---
title: "CMFCCaptionBar::OnDrawButton"
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
ms.assetid: fd93f136-7d07-4113-8510-d2bc02c9f54d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCaptionBar::OnDrawButton
Called by the framework to draw the caption bar button.  
  
## Syntax  
  
```  
virtual void OnDrawButton(  
   CDC* pDC,  
   CRect rect,  
   const CString& strButton,  
   BOOL bEnabled   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context that is used to display the button.  
  
 [in] `rect`  
 The bounding rectangle of the button.  
  
 [in] `strButton`  
 The button's text label.  
  
 [in] `bEnabled`  
 `TRUE` if the button is enabled; `FALSE` otherwise.  
  
## Remarks  
 Override this method in a `CMFCCaptionBar` derived class to customize the appearance of the caption bar's button.  
  
## Requirements  
 **Header:** afxcaptionbar.h  
  
## See Also  
 [CMFCCaptionBar Class](../vs140/CMFCCaptionBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)