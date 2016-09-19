---
title: "CMDIFrameWndEx::OnCmdMsg"
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
ms.assetid: b06a1feb-d287-464e-b147-692577b2fc8c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::OnCmdMsg
Called by the framework to route and dispatch command messages and to update command user-interface objects.  
  
## Syntax  
  
```  
virtual BOOL OnCmdMsg(  
   UINT nID,  
   int nCode,  
   void* pExtra,  
   AFX_CMDHANDLERINFO* pHandlerInfo  
);  
```  
  
#### Parameters  
 [in] `nID`  
 The command ID.  
  
 [in] `nCode`  
 Identifies the command notification code. See [CCmdTarget::OnCmdMsg](../vs140/CCmdTarget--OnCmdMsg.md) for more information about values for `nCode`.  
  
 [in] `pExtra`  
 Used according to the value of `nCode`. See [CCmdTarget::OnCmdMsg](../vs140/CCmdTarget--OnCmdMsg.md) for more information about `pExtra`.  
  
 [in, out] `pHandlerInfo`  
 Typically, this parameter should be `NULL`.If not `NULL`, `OnCmdMsg` fills in the `pTarget` and `pmf` members of the `pHandlerInfo` structure instead of dispatching the command.  
  
## Return Value  
 Nonzero if the message is handled; otherwise 0.  
  
## Requirements  
 **Header:** afxmdiframewndex.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CCmdTarget::OnCmdMsg](../vs140/CCmdTarget--OnCmdMsg.md)