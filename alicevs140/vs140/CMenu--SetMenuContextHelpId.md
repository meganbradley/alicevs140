---
title: "CMenu::SetMenuContextHelpId"
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
ms.assetid: 419a61c5-7671-4a5c-96b9-181e4decfbb0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::SetMenuContextHelpId
Associates a context help ID with `CMenu`.  
  
## Syntax  
  
```  
  
      BOOL SetMenuContextHelpId(  
   DWORD dwContextHelpId   
);  
```  
  
#### Parameters  
 `dwContextHelpId`  
 Context help ID to associate with `CMenu`.  
  
## Return Value  
 Nonzero if successful; otherwise 0  
  
## Remarks  
 All items in the menu share this identifier — it is not possible to attach a help context identifier to the individual menu items.  
  
## Example  
 See the example for [CMenu::InsertMenu](../vs140/CMenu--InsertMenu.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::GetMenuContextHelpId](../vs140/CMenu--GetMenuContextHelpId.md)   
 [SetMenuContextHelpId](http://msdn.microsoft.com/library/windows/desktop/bb762099)