---
title: "CMFCColorButton::SetDocumentColors"
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
ms.assetid: 5cfc870d-e04e-4552-ae3f-60f1e60cad9f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorButton::SetDocumentColors
Specifies a set of colors and the set's name. The set of colors is displayed using a [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md) object.  
  
## Syntax  
  
```  
void SetDocumentColors(  
   LPCTSTR lpszLabel,  
   CList<COLORREF,COLORREF>& lstColors   
);  
```  
  
#### Parameters  
 [in] `lpszLabel`  
 Specifies the label to be displayed with the set of document colors.  
  
 [in] `lstColors`  
 A reference to a list of RGB values.  
  
## Remarks  
 A `CMFCColorButton` object maintains a list of RGB values that are transferred to a [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md) object. When the color bar is displayed, these colors are shown in a special section whose label is specified by the `lpszLabel` parameter.  
  
## Requirements  
 **Header:** afxcolorbutton.h  
  
## See Also  
 [CMFCColorButton Class](../vs140/CMFCColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)