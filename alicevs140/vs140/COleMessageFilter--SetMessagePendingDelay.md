---
title: "COleMessageFilter::SetMessagePendingDelay"
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
ms.assetid: b5d87f73-f8cb-4258-971e-444ae755f319
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleMessageFilter::SetMessagePendingDelay
Determines how long the calling application waits for a response from the called application before taking further action.  
  
## Syntax  
  
```  
  
      void SetMessagePendingDelay(  
   DWORD nTimeout = 5000   
);  
```  
  
#### Parameters  
 `nTimeout`  
 Number of milliseconds for the message-pending delay.  
  
## Remarks  
 This function works in concert with [SetRetryReply](../vs140/COleMessageFilter--SetRetryReply.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleMessageFilter Class](../vs140/COleMessageFilter-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleMessageFilter::SetRetryReply](../vs140/COleMessageFilter--SetRetryReply.md)