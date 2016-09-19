---
title: "COleMessageFilter::SetBusyReply"
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
ms.assetid: c35dd858-f04f-4e5e-81f7-cbeedafb5ab6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleMessageFilter::SetBusyReply
This function sets the application's "busy reply."  
  
## Syntax  
  
```  
  
      void SetBusyReply(  
   SERVERCALL nBusyReply   
);  
```  
  
#### Parameters  
 *nBusyReply*  
 A value from the `SERVERCALL` enumeration, which is defined in COMPOBJ.H. It can have any one of the following values:  
  
-   **SERVERCALL_ISHANDLED** The application can accept calls but may fail in processing a particular call.  
  
-   **SERVERCALL_REJECTED** The application probably will never be able to process a call.  
  
-   **SERVERCALL_RETRYLATER** The application is temporarily in a state in which it cannot process a call.  
  
## Remarks  
 The [BeginBusyState](../vs140/COleMessageFilter--BeginBusyState.md) and [EndBusyState](../vs140/COleMessageFilter--EndBusyState.md) functions control the application's busy state.  
  
 When an application has been made busy with a call to `BeginBusyState`, it responds to calls from the OLE system DLLs with a value determined by the last setting of `SetBusyReply`. The calling application uses this busy reply to determine what action to take.  
  
 By default, the busy reply is **SERVERCALL_RETRYLATER**. This reply causes the calling application to retry the call as soon as possible.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleMessageFilter Class](../vs140/COleMessageFilter-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleMessageFilter::BeginBusyState](../vs140/COleMessageFilter--BeginBusyState.md)   
 [COleMessageFilter::EndBusyState](../vs140/COleMessageFilter--EndBusyState.md)