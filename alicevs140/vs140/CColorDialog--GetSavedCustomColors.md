---
title: "CColorDialog::GetSavedCustomColors"
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
ms.assetid: 18467303-9aef-45f0-b21e-bcda8936deb9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CColorDialog::GetSavedCustomColors
`CColorDialog` objects permit the user, in addition to choosing colors, to define up to 16 custom colors.  
  
## Syntax  
  
```  
  
static COLORREF * PASCAL GetSavedCustomColors( );  
```  
  
## Return Value  
 A pointer to an array of 16 RGB color values that stores custom colors created by the user.  
  
## Remarks  
 The `GetSavedCustomColors` member function provides access to these colors. These colors can be retrieved after [DoModal](../vs140/CColorDialog--DoModal.md) returns **IDOK**.  
  
 Each of the 16 RGB values in the returned array is initialized to RGB(255,255,255) (white). The custom colors chosen by the user are saved only between dialog box invocations within the application. If you wish to save these colors between invocations of the application, you must save them in some other manner, such as in an initialization (.INI) file.  
  
## Example  
 [!CODE [NVC_MFCDocView#51](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#51)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CColorDialog Class](../vs140/CColorDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CColorDialog::GetColor](../vs140/CColorDialog--GetColor.md)