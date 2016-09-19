---
title: "CMDIChildWndEx::SetTaskbarTabOrder"
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
ms.assetid: 4aa73c91-ade4-41d7-ae61-547a804ed172
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::SetTaskbarTabOrder
Inserts the MDI child before the specified window on Windows 7 taskbar tabs.  
  
## Syntax  
  
```  
void SetTaskbarTabOrder(  
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