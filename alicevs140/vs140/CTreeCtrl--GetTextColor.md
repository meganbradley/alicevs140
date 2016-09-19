---
title: "CTreeCtrl::GetTextColor"
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
ms.assetid: 4b56b22d-74f1-486f-bba5-a77056d1a8b3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::GetTextColor
This member function implements the behavior of the Win32 message [TVM_GETTEXTCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb773633), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
COLORREF GetTextColor( ) const;  
  
```  
  
## Return Value  
 A **COLORREF** value that represents the current text color. If this value is -1, the control is using the system color for the text color.  
  
## Example  
 See the example for [CTreeCtrl::SetTextColor](../vs140/CTreeCtrl--SetTextColor.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::SetTextColor](../vs140/CTreeCtrl--SetTextColor.md)