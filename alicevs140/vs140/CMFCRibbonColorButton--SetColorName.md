---
title: "CMFCRibbonColorButton::SetColorName"
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
ms.assetid: 2519aac3-c265-49ee-8a53-a342acb2d107
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonColorButton::SetColorName
Sets a new name for a specified color.  
  
## Syntax  
  
```  
static void __stdcall SetColorName(  
   COLORREF color,  
   const CString& strName  
);  
```  
  
#### Parameters  
 [in] `color`  
 The RGB value of a color.  
  
 [in] `strName`  
 The new name for the specified color.  
  
## Remarks  
 Because it calls `CMFCColorBar::SetColorName`, this method changes the name of the specified color in all `CMFCColorBar` objects in your application.  
  
## Requirements  
 **Header:** afxribboncolorbutton.h  
  
## See Also  
 [CMFCRibbonColorButton Class](../vs140/CMFCRibbonColorButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)