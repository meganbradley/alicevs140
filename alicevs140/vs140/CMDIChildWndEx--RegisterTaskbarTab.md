---
title: "CMDIChildWndEx::RegisterTaskbarTab"
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
ms.assetid: b7b8aebb-4a81-4a20-a894-54671d8c74b1
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::RegisterTaskbarTab
Registers the MDI child with Windows 7 taskbar tabs.  
  
## Syntax  
  
```  
virtual void RegisterTaskbarTab(  
   CMDIChildWndEx* pWndBefore = NULL  
);  
```  
  
#### Parameters  
 `pWndBefore`  
 A pointer to the MDI child window whose thumbnail is inserted to the left. This window must already be registered through `RegisterTaskbarTab`. If this value is `NULL`, the new thumbnail is added to the end of the list.  
  
## Remarks  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)