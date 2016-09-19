---
title: "CFrameWndEx::SetupToolbarMenu"
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
ms.assetid: 1c205b44-de8f-45f4-8633-3cc098b22282
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::SetupToolbarMenu
Inserts user-defined commands into a toolbar menu.  
  
## Syntax  
  
```  
void SetupToolbarMenu(  
   CMenu& menu,  
   const UINT uiViewUserToolbarCmdFirst,  
   const UINT uiViewUserToolbarCmdLast  
);  
```  
  
#### Parameters  
 [in] `menu`  
 A `CMenu` object to be modified.  
  
 [in] `uiViewUserToolbarCmdFirst`  
 The first user-defined command.  
  
 [in] `uiViewUserToolbarCmdLast`  
 The last user-defined command.  
  
## Remarks  
 The framework stores user-defined commands in a list. Use `uiViewUserToolbarCmdFirst` and `uiViewUserToolbarCmdList` to specify the indexes of the commands to insert.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)