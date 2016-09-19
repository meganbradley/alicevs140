---
title: "CMenu::Attach"
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
ms.assetid: a0d98596-ca75-4326-9c6c-b75f0bccee09
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::Attach
Attaches an existing Windows menu to a `CMenu` object.  
  
## Syntax  
  
```  
  
      BOOL Attach(  
   HMENU hMenu   
);  
```  
  
#### Parameters  
 `hMenu`  
 Specifies a handle to a Windows menu.  
  
## Return Value  
 Nonzero if the operation was successful; otherwise 0.  
  
## Remarks  
 This function should not be called if a menu is already attached to the `CMenu` object. The menu handle is stored in the `m_hMenu` data member.  
  
 If the menu you want to manipulate is already associated with a window, you can use the [CWnd::GetMenu](../vs140/CWnd--GetMenu.md) function to get a handle to the menu.  
  
## Example  
 [!CODE [NVC_MFCWindowing#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#21)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::Detach](../vs140/CMenu--Detach.md)   
 [CMenu::CMenu](../vs140/CMenu--CMenu.md)   
 [CWnd::GetMenu](../vs140/CWnd--GetMenu.md)