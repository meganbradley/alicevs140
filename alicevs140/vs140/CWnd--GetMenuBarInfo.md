---
title: "CWnd::GetMenuBarInfo"
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
ms.assetid: 621fdb41-b2de-4c6e-be20-4774709025d8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetMenuBarInfo
Retrieves information about the specified menu bar.  
  
## Syntax  
  
```  
  
      BOOL GetMenuBarInfo(  
   LONG idObject,  
   LONG idItem,  
   PMENUBARINFO pmbi  
) const;  
```  
  
#### Parameters  
 `idObject`  
 Specifies the menu object. For a list of possible values, see [GetMenuBarInfo](http://msdn.microsoft.com/library/windows/desktop/ms647833).  
  
 `idItem`  
 Specifies the item for which to retrieve information. If this parameter is zero, the function retrieves information about the menu itself. If this parameter is 1, the function retrieves information about the first item on the menu, and so on.  
  
 *pmbi*  
 Pointer to a [MENUBARINFO](http://msdn.microsoft.com/library/windows/desktop/ms647564) structure that receives the information.  
  
## Return Value  
 Nonzero if the function succeeds; otherwise 0.  
  
## Remarks  
 This member function emulates the functionality of the function [GetMenuBarInfo](http://msdn.microsoft.com/library/windows/desktop/ms647833), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)