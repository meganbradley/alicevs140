---
title: "CMFCPropertyGridColorProperty::EnableOtherButton"
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
ms.assetid: b733c3df-dd16-4a4f-b6ae-a02d450e0fea
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridColorProperty::EnableOtherButton
Enables the *other* button on the color selection dialog box. (The standard other button is labeled **More Colors…**.)  
  
## Syntax  
  
```  
void EnableOtherButton(  
   LPCTSTR lpszLabel,  
   BOOL bAltColorDlg = TRUE,  
   BOOL bEnable = TRUE   
);  
```  
  
#### Parameters  
 [in] `lpszLabel`  
 The label text of the other button.  
  
 [in] `bAltColorDlg`  
 `TRUE` to display the `CMFCColorDialog` dialog box; `FALSE` to display the standard color selection dialog box. The default value is `TRUE`.  
  
 [in] `bEnable`  
 `TRUE` to display the other button; otherwise, `FALSE`.  The default value is `TRUE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridColorProperty Class](../vs140/CMFCPropertyGridColorProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)