---
title: "COccManager::OnEvent"
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
ms.assetid: 273badaf-8de1-4444-a00c-6a262eb7277a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COccManager::OnEvent
Called by the framework to handle the specified event.  
  
## Syntax  
  
```  
  
      virtual BOOL OnEvent(  
   CCmdTarget* pCmdTarget,  
   UINT idCtrl,  
   AFX_EVENT* pEvent,  
   AFX_CMDHANDLERINFO* pHandlerInfo   
);  
```  
  
#### Parameters  
 *pCmdTarget*  
 A pointer to the `CCmdTarget` object attempting to handle the event  
  
 `idCtrl`  
 The resource ID of the control.  
  
 `pEvent`  
 The event being handled.  
  
 `pHandlerInfo`  
 If not **NULL**, `OnEvent` fills in the **pTarget** and **pmf** members of the **AFX_CMDHANDLERINFO** structure instead of dispatching the command. Typically, this parameter should be **NULL**.  
  
## Return Value  
 Nonzero if the event was handled, otherwise zero.  
  
## Remarks  
 Override this function to customize the default event-handling process.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COccManager Class](../vs140/COccManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)