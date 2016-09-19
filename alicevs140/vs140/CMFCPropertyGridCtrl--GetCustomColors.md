---
title: "CMFCPropertyGridCtrl::GetCustomColors"
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
ms.assetid: 458d150f-01fb-49af-adec-5d225a4f74b6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::GetCustomColors
Retrieves the custom colors that are currently defined for property grid control elements.  
  
## Syntax  
  
```  
void GetCustomColors(  
   COLORREF& clrBackground,  
   COLORREF& clrText,  
   COLORREF& clrGroupBackground,  
   COLORREF& clrGroupText,  
   COLORREF& clrDescriptionBackground,  
   COLORREF& clrDescriptionText,  
   COLORREF& clrLine   
);  
```  
  
#### Parameters  
 [out] `clrBackground`  
 The background color of property values.  
  
 [out] `clrText`  
 The color of property names and property value text.  
  
 [out] `clrGroupBackground`  
 The background color of a property group.  
  
 [out] `clrGroupText`  
 The color of text in the property group.  
  
 [out] `clrDescriptionBackground`  
 The background color of the description area.  
  
 [out] `clrDescriptionText`  
 The color of text in the description area.  
  
 [out] `clrLine`  
 The color of lines that are drawn between properties.  
  
## Remarks  
 Use the [CMFCPropertyGridCtrl::SetCustomColors](../vs140/CMFCPropertyGridCtrl--SetCustomColors.md) method to set custom colors.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridCtrl::SetCustomColors](../vs140/CMFCPropertyGridCtrl--SetCustomColors.md)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)