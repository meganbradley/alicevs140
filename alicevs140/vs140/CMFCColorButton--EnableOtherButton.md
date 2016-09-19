---
title: "CMFCColorButton::EnableOtherButton"
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
ms.assetid: e727c983-9cf9-47b9-8aa3-8d0b43071203
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorButton::EnableOtherButton
Enable or disable the "other" button, which appears below regular color buttons.  
  
## Syntax  
  
```  
void EnableOtherButton(  
   LPCTSTR lpszLabel,  
   BOOL bAltColorDlg=TRUE,  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `lpszLabel`  
 Specifies the button's text.  
  
 [in] `bAltColorDlg`  
 Specifies whether the [CMFCColorDialog](../vs140/CMFCColorDialog-Class.md) dialog box or the system color dialog box is opened when the user clicks the button.  
  
 [in] `bEnable`  
 Specifies whether the "other" button is enabled or disabled.  
  
## Remarks  
 Click the "other" button to display a color dialog box. If the *bAltColorDlg* parameter is `TRUE`, the [CMFCColorDialog Class](../vs140/CMFCColorDialog-Class.md) is displayed; otherwise, the system color dialog box is displayed.  
  
## Requirements  
 **Header:** afxcolorbutton.h  
  
## See Also  
 [CMFCColorButton Class](../vs140/CMFCColorButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)