---
title: "CMFCRibbonCheckBox::OnDrawMenuImage"
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
ms.assetid: ae1f6fb6-5663-41e8-a2fb-2ff120132eac
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCheckBox::OnDrawMenuImage
Called by the framework to draw a menu image for the checkbox.  
  
## Syntax  
  
```  
virtual BOOL OnDrawMenuImage(  
    CDC*,  
    CRect  
);  
```  
  
#### Parameters  
 [in] `CDC*`  
 Pointer to the `CDC` associated with the checkbox.  
  
 [in] `CRect`  
 A `CRect` object specifying the rectangle in which to draw the menu image.  
  
## Return Value  
 Returns `TRUE` if the image was drawn, or `FALSE` if not.  
  
## Remarks  
 If not overridden, returns `FALSE`.  
  
## Requirements  
 **Header:** afxribboncheckbox.h  
  
## See Also  
 [CMFCRibbonCheckBox Class](../vs140/CMFCRibbonCheckBox-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)