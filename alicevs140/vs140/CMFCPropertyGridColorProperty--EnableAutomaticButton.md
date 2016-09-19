---
title: "CMFCPropertyGridColorProperty::EnableAutomaticButton"
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
ms.assetid: 360104d8-294a-47d8-acb8-35942cc26b46
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridColorProperty::EnableAutomaticButton
Enables the *automatic* button on the color selection dialog box. (The standard automatic button is labeled **Automatic**.)  
  
## Syntax  
  
```  
void EnableAutomaticButton(  
   LPCTSTR lpszLabel,  
   COLORREF colorAutomatic,  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `lpszLabel`  
 The label text of the automatic button.  
  
 [in] `colorAutomatic`  
 The RGB color value of the automatic (default) color.  
  
 [in] `bEnable`  
 `TRUE` to enable the automatic button; otherwise, `FALSE`. The default value is `TRUE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridColorProperty Class](../vs140/CMFCPropertyGridColorProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)