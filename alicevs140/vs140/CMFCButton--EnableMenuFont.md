---
title: "CMFCButton::EnableMenuFont"
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
ms.assetid: 8bbd47be-2daa-47c2-9c35-a9440eaa7dcc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCButton::EnableMenuFont
Specifies whether the button text font is the same as the application menu font.  
  
## Syntax  
  
```  
void EnableMenuFont(  
   BOOL bOn=TRUE,  
   BOOL bRedraw=TRUE   
);  
```  
  
#### Parameters  
 [in] `bOn`  
 `TRUE` to use the application menu font as the button text font; `FALSE` to use the system font. The default is `TRUE`.  
  
 [in] `bRedraw`  
 `TRUE` to immediately redraw the screen; otherwise, `FALSE`. The default is `TRUE`.  
  
## Remarks  
 If you do not use this method to specify the button text font, you can specify the font with the [CWnd::SetFont](../vs140/CWnd--SetFont.md) method. If you do not specify a font at all, the framework sets a default font.  
  
## Requirements  
 **Header:** afxbutton.h  
  
## See Also  
 [CMFCButton Class](../vs140/CMFCButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)