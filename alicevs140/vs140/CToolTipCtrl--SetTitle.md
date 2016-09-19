---
title: "CToolTipCtrl::SetTitle"
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
ms.assetid: 7e2cee33-20bd-42fe-9173-12289f72fd89
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::SetTitle
Adds a standard icon and title string to a tool tip.  
  
## Syntax  
  
```  
  
      BOOL SetTitle(  
   UINT uIcon,  
   LPCTSTR lpstrTitle   
);  
```  
  
#### Parameters  
 *uIcon*  
 See *icon* in [TTM_SETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760414) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 *lpstrTitle*  
 Pointer to the title string.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TTM_SETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760414), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)