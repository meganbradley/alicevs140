---
title: "CReBarCtrl::SetWindowTheme"
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
ms.assetid: 513eff6d-fcc9-4f7c-b466-384b47c5c283
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::SetWindowTheme
Sets the visual style of the rebar control.  
  
## Syntax  
  
```  
  
      HRESULT SetWindowTheme(   
   LPCWSTR pszSubAppName    
);  
```  
  
#### Parameters  
 `pszSubAppName`  
 A pointer to a Unicode string that contains the rebar visual style to set.  
  
## Return Value  
 The return value is not used.  
  
## Remarks  
 This member function emulates the functionality of the [RB_SETWINDOWTHEME](http://msdn.microsoft.com/library/windows/desktop/bb774530) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)