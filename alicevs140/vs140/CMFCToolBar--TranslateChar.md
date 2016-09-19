---
title: "CMFCToolBar::TranslateChar"
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
ms.assetid: 8e09a839-3607-4898-b11b-4e188e4cb54e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::TranslateChar
Executes a button command if the specified key code corresponds to a valid keyboard shortcut.  
  
## Syntax  
  
```  
virtual BOOL TranslateChar(  
   UINT nChar  
);  
```  
  
#### Parameters  
 [in] `nChar`  
 Specifies a virtual key code. For a list of standard virtual key codes, see Winuser.h  
  
## Return Value  
 `FALSE` if the specified key code is either unprintable or does not correspond to a valid keyboard shortcut; `TRUE` if the specified key code corresponds to a drop-down menu option; otherwise, the return value from [CMFCToolBar::ProcessCommand](../vs140/CMFCToolBar--ProcessCommand.md).  
  
## Remarks  
 The framework calls this method when a key is pressed together with the Alt key.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)