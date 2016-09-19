---
title: "CMFCColorButton::OnDrawFocusRect"
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
ms.assetid: 5568d981-572f-4722-be9a-207560ab0543
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorButton::OnDrawFocusRect
Called by the framework to display a focus rectangle when the button has focus.  
  
## Syntax  
  
```  
virtual void OnDrawFocusRect(  
   CDC* pDC,  
   const CRect& rectClient   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Points to the device context used to draw the focus rectangle.  
  
 [in] `rectClient`  
 A rectangle in the device context specified by the `pDC` parameter that defines the boundaries of the button.  
  
## Remarks  
 Override this method to customize appearance of the focus rectangle.  
  
## Requirements  
 **Header:** afxcolorbutton.h  
  
## See Also  
 [CMFCColorButton Class](../vs140/CMFCColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)