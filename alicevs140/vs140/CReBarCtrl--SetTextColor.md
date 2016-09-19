---
title: "CReBarCtrl::SetTextColor"
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
ms.assetid: 80a694d8-7930-4aef-97bb-63ad27c14b01
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::SetTextColor
Implements the behavior of the Win32 message [RB_SETTEXTCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb774524), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      COLORREF SetTextColor(  
   COLORREF clr   
);  
```  
  
#### Parameters  
 `clr`  
 A **COLORREF** value that represents the new text color in the `CReBarCtrl` object.  
  
## Return Value  
 The [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value representing the previous text color associated with the `CReBarCtrl` object.  
  
## Remarks  
 It is provided to support text color flexibility in a rebar control.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::GetTextColor](../vs140/CReBarCtrl--GetTextColor.md)