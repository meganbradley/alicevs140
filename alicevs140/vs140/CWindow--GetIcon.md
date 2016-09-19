---
title: "CWindow::GetIcon"
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
ms.assetid: e05604ce-8def-4056-b37b-ad528ff7cca0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetIcon
Retrieves the handle to the window's large or small icon.  
  
## Syntax  
  
```  
  
HICON GetIcon( BOOL   
bBigIcon  
 = TRUE ) const;  
  
```  
  
#### Parameters  
 `bBigIcon`  
 [in] If **TRUE** (the default value) the method returns the large icon. Otherwise, it returns the small icon.  
  
## Return Value  
 An icon handle.  
  
## Remarks  
 `GetIcon` sends a [WM_GETICON](http://msdn.microsoft.com/library/windows/desktop/ms632625) message to the window.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetIcon](../vs140/CWindow--SetIcon.md)