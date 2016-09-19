---
title: "CMDIFrameWndEx::SetupToolbarMenu"
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
ms.assetid: 79af6985-2c76-4b17-a24e-1748125311e7
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::SetupToolbarMenu
Modifies a toolbar object by replacing dummy items with user-defined items.  
  
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
 A reference to a [CMenu Class](../vs140/CMenu-Class.md) object to be modified.  
  
 [in] `uiViewUserToolbarCmdFirst`  
 Specifies the first user-defined command.  
  
 [in] `uiViewUserToolbarCmdLast`  
 Specifies the last user-defined command.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)