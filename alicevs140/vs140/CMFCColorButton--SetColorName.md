---
title: "CMFCColorButton::SetColorName"
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
ms.assetid: 0d3771ef-ffd5-4219-9383-11ffad962a3b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorButton::SetColorName
Specifies the name of a color.  
  
## Syntax  
  
```  
static void SetColorName(  
   COLORREF color,  
   const CString& strName   
);  
```  
  
#### Parameters  
 [in] `color`  
 The color's RGB value.  
  
 [in] `strName`  
 The color's name.  
  
## Remarks  
 The list of color names is global per application. Consequently, this method transfers its parameters to [CMFCColorBar::SetColorName](../vs140/CMFCColorBar--SetColorName.md).  
  
## Requirements  
 **Header:** afxcolorbutton.h  
  
## See Also  
 [CMFCColorButton Class](../vs140/CMFCColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)