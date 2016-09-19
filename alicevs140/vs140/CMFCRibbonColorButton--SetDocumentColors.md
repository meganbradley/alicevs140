---
title: "CMFCRibbonColorButton::SetDocumentColors"
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
ms.assetid: 44f718fb-cad4-4ace-92e7-41ef449660c8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonColorButton::SetDocumentColors
Specifies a list of RGB values to display in the document color area.  
  
## Syntax  
  
```  
void SetDocumentColors(  
   LPCTSTR lpszLabel,  
   CList<COLORREF,COLORREF>& lstColors   
);  
```  
  
#### Parameters  
 [in] `lpszLabel`  
 The text to be displayed with the document colors.  
  
 [in] `lstColors`  
 A reference to a list of RGB values.  
  
## Requirements  
 **Header:** afxribboncolorbutton.h  
  
## See Also  
 [CMFCRibbonColorButton Class](../vs140/CMFCRibbonColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)