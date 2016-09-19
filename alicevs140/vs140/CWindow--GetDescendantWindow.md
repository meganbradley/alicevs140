---
title: "CWindow::GetDescendantWindow"
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
ms.assetid: 0daa7bad-1529-4e2c-af90-d01b1e290abc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetDescendantWindow
Finds the descendant window specified by the given identifier.  
  
## Syntax  
  
```  
  
      HWND GetDescendantWindow(  
   int nID   
) const throw();  
```  
  
#### Parameters  
 `nID`  
 [in] The identifier of the descendant window to be retrieved.  
  
## Return Value  
 The handle to a descendant window.  
  
## Remarks  
 `GetDescendantWindow` searches the entire tree of child windows, not only the windows that are immediate children.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetDlgItem](../vs140/CWindow--GetDlgItem.md)