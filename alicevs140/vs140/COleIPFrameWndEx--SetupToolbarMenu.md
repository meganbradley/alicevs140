---
title: "COleIPFrameWndEx::SetupToolbarMenu"
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
ms.assetid: 68ae4b28-6274-4d41-a35e-61801382c00b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::SetupToolbarMenu
Modifies a toolbar object by searching for dummy items and replacing them with the specified user-defined items.  
  
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
 A reference to a [CMenu](../vs140/CMenu-Class.md) object to be modified.  
  
 [in] `uiViewUserToolbarCmdFirst`  
 Specifies the first user-defined command.  
  
 [in] `uiViewUserToolbarCmdLast`  
 Specifies the last user-defined command.  
  
## Remarks  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)