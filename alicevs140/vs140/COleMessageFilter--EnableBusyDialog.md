---
title: "COleMessageFilter::EnableBusyDialog"
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
ms.assetid: ee491d92-d85b-496a-96ba-88a16b0173b3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleMessageFilter::EnableBusyDialog
Enables and disables the busy dialog box, which is displayed when the message-pending delay expires (see [SetRetryReply](../vs140/COleMessageFilter--SetRetryReply.md)) during an OLE call.  
  
## Syntax  
  
```  
  
      void EnableBusyDialog(  
   BOOL bEnableBusy = TRUE   
);  
```  
  
#### Parameters  
 *bEnableBusy*  
 Specifies whether the "busy" dialog box is enabled or disabled.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleMessageFilter Class](../vs140/COleMessageFilter-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleMessageFilter::EnableNotRespondingDialog](../vs140/COleMessageFilter--EnableNotRespondingDialog.md)   
 [COleMessageFilter::BeginBusyState](../vs140/COleMessageFilter--BeginBusyState.md)   
 [COleMessageFilter::SetBusyReply](../vs140/COleMessageFilter--SetBusyReply.md)   
 [COleMessageFilter::SetRetryReply](../vs140/COleMessageFilter--SetRetryReply.md)   
 [COleBusyDialog Class](../vs140/COleBusyDialog-Class.md)