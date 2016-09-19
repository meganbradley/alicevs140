---
title: "CStatusBarCtrl::IsSimple"
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
ms.assetid: 26828d14-0fa5-4b00-8c13-3c5c9f5a36a5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::IsSimple
Checks a status window control to determine if it is in simple mode.  
  
## Syntax  
  
```  
  
BOOL IsSimple( ) const;  
  
```  
  
## Return Value  
 Nonzero if the status window control is in simple mode; otherwise zero.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [SB_ISSIMPLE](http://msdn.microsoft.com/library/windows/desktop/bb760753), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBarCtrl Class](../vs140/CStatusBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBarCtrl::SetSimple](../vs140/CStatusBarCtrl--SetSimple.md)