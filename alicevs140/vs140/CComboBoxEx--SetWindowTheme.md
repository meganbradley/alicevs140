---
title: "CComboBoxEx::SetWindowTheme"
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
ms.assetid: 17868d07-051f-45b3-bb11-8b58919db07b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBoxEx::SetWindowTheme
Sets the visual style of the extended combo box control.  
  
## Syntax  
  
```  
  
      HRESULT SetWindowTheme(  
   LPCWSTR pszSubAppName   
);  
```  
  
#### Parameters  
 `pszSubAppName`  
 A pointer to a Unicode string that contains the extended combo box visual style to set.  
  
## Return Value  
 The return value is not used.  
  
## Remarks  
 This member function emulates the functionality of the [CBEM_SETWINDOWTHEME](http://msdn.microsoft.com/library/windows/desktop/bb775790) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CComboBoxEx Class](../vs140/CComboBoxEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)