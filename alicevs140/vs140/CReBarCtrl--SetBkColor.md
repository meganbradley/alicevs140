---
title: "CReBarCtrl::SetBkColor"
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
ms.assetid: 6ab3690c-922a-499e-be5c-8eb264897d83
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::SetBkColor
Implements the behavior of the Win32 message [RB_SETBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb774515), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      COLORREF SetBkColor(  
   COLORREF clr   
);  
```  
  
#### Parameters  
 `clr`  
 The **COLORREF** value that represents the new default background color.  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value that represents the previous default background color.  
  
## Remarks  
 See this topic for more information about when to set the background color, and how to set the default.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::GetBkColor](../vs140/CReBarCtrl--GetBkColor.md)