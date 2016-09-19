---
title: "CMFCRibbonEdit::CMFCRibbonEdit"
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
ms.assetid: b38cd4e6-8844-4b4f-9b3d-8ac8d3d7715f
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonEdit::CMFCRibbonEdit
Constructs a [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) object.  
  
## Syntax  
  
```  
CMFCRibbonEdit(  
   UINT nID,  
   int nWidth,  
   LPCTSTR lpszLabel = NULL,  
   int nImage = -1  
);  
CMFCRibbonEdit();  
```  
  
#### Parameters  
 [in] `nID`  
 Command ID for the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control.  
  
 [in] `nWidth`  
 The width, in pixels, of the text box for the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control.  
  
 [in] `lpszLabel`  
 The label for the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control.  
  
 [in] `nImage`  
 Index of the small image to use for the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control. The collection of small images is maintained by the parent ribbon category.  
  
## Remarks  
 The [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control does not use a large image.  
  
## Requirements  
 **Header:** afxribbonedit.h  
  
## See Also  
 [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)