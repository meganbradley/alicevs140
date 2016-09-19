---
title: "CToolTipCtrl::SetTipTextColor"
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
ms.assetid: 179613d2-a158-4a39-a1ba-1488b7b74de3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::SetTipTextColor
Sets the text color in a tool tip window.  
  
## Syntax  
  
```  
  
      void SetTipTextColor(  
   COLORREF clr   
);  
```  
  
#### Parameters  
 `clr`  
 The new text color.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TTM_SETTIPTEXTCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760413), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::GetTipTextColor](../vs140/CToolTipCtrl--GetTipTextColor.md)