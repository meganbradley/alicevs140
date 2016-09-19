---
title: "CMFCPropertyGridFontProperty::CMFCPropertyGridFontProperty"
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
ms.assetid: 7fdb39f2-2aa7-4961-934b-fece05fbdfee
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridFontProperty::CMFCPropertyGridFontProperty
Constructs a `CMFCPropertyGridFontProperty` object.  
  
## Syntax  
  
```  
CMFCPropertyGridFontProperty(  
   const CString& strName,  
   LOGFONT& lf,  
   DWORD dwFontDialogFlags = CF_EFFECTS | CF_SCREENFONTS,  
   LPCTSTR lpszDescr = NULL,  
   DWORD_PTR dwData = 0,  
   COLORREF color = (COLORREF)-1  
);  
```  
  
#### Parameters  
 [in] `strName`  
 The name of the property.  
  
 [in] `lf`  
 A logical font structure that specifies the attributes of the font.  
  
 [in] `dwFontDialogFlags`  
 Styles that are applied to the font dialog box that is displayed when you click the property value drop-down button. The default value is the bitwise combination (OR) of CF_EFFECTS and CF_SCREENFONTS. For more information, see the `Flags` parameter of the [CHOOSEFONT Structure](http://msdn.microsoft.com/library/windows/desktop/ms646832).  
  
 [in] `lpszDescr`  
 Description of the font property. The default value is `NULL`.  
  
 [in] `dwData`  
 Application-specific data, such as an integer or a pointer to other data that is associated with the property. The default value is 0.  
  
 [in] `color`  
 The color of the font. The default value is the default color.  
  
## Remarks  
 A `CMFCPropertyGridFontProperty` object represents a font property in a property grid font control.  
  
## Example  
 The following example demonstrates how construct an object of the `CMFCPropertyGridFontProperty` class. This example is part of the [New Controls sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_NewControls#26](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#26)]  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridFontProperty Class](../vs140/CMFCPropertyGridFontProperty-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [LOGFONT](http://msdn.microsoft.com/library/windows/desktop/bb773327)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)