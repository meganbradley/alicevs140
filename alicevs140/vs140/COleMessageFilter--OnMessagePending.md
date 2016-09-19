---
title: "COleMessageFilter::OnMessagePending"
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
ms.assetid: 0b912a69-9fd9-4ac3-accf-f8a1c2c407ad
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleMessageFilter::OnMessagePending
Called by the framework to process messages while an OLE call is in progress.  
  
## Syntax  
  
```  
  
      virtual BOOL OnMessagePending(  
   const MSG* pMsg   
);  
```  
  
#### Parameters  
 `pMsg`  
 Pointer to the pending message.  
  
## Return Value  
 Nonzero on success; otherwise 0.  
  
## Remarks  
 When a calling application is waiting for a call to be completed, the framework calls `OnMessagePending` with a pointer to the pending message. By default, the framework dispatches `WM_PAINT` messages, so that window updates can occur during a call that is taking a long time.  
  
 You must register your message filter by means of a call to [Register](../vs140/COleMessageFilter--Register.md) before it can become active.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleMessageFilter Class](../vs140/COleMessageFilter-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleMessageFilter::Register](../vs140/COleMessageFilter--Register.md)   
 [AfxOleInit](../vs140/AfxOleInit.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)