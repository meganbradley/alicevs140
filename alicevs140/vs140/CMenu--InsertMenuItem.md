---
title: "CMenu::InsertMenuItem"
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
ms.assetid: 61d8033b-cb10-49ae-b45f-2dc3df05db0b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::InsertMenuItem
Inserts a new menu item at the specified position in a menu.  
  
## Syntax  
  
```  
  
      BOOL InsertMenuItem(  
   UINT uItem,  
   LPMENUITEMINFO lpMenuItemInfo,  
   BOOL fByPos = FALSE  
);  
```  
  
#### Parameters  
 `uItem`  
 See description of `uItem` in [InsertMenuItem](http://msdn.microsoft.com/library/windows/desktop/ms647988) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `lpMenuItemInfo`  
 See description of `lpmii` in **InsertMenuItem** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `fByPos`  
 See description of `fByPosition` in **InsertMenuItem** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 This function wraps [InsertMenuItem](http://msdn.microsoft.com/library/windows/desktop/ms647988), described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)