---
title: "CToolBarCtrl::SetWindowTheme"
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
ms.assetid: 527c2573-8637-4a5f-9eca-b0ac35f64db3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetWindowTheme
Sets the visual style of the `CToolBarCtrl` object.  
  
## Syntax  
  
```  
  
      HRESULT SetWindowTheme(  
   LPCWSTR pszSubAppName  
);  
```  
  
#### Parameters  
 `pszSubAppName`  
 A pointer to a Unicode string that contains the toolbar visual style to set.  
  
## Return Value  
 The return value is not used.  
  
## Remarks  
 This member function emulates the functionality of the [TB_SETWINDOWTHEME](http://msdn.microsoft.com/library/windows/desktop/bb787465) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)