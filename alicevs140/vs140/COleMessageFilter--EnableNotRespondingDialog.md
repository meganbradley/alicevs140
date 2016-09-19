---
title: "COleMessageFilter::EnableNotRespondingDialog"
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
ms.assetid: 9b2f04ac-4e9d-41c8-83ba-c9b571ee835a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleMessageFilter::EnableNotRespondingDialog
Enables and disables the "not responding" dialog box, which is displayed if a keyboard or mouse message is pending during an OLE call and the call has timed out.  
  
## Syntax  
  
```  
  
      void EnableNotRespondingDialog(  
   BOOL bEnableNotResponding = TRUE   
);  
```  
  
#### Parameters  
 *bEnableNotResponding*  
 Specifies whether the "not responding" dialog box is enabled or disabled.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleMessageFilter Class](../vs140/COleMessageFilter-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleMessageFilter::EnableBusyDialog](../vs140/COleMessageFilter--EnableBusyDialog.md)   
 [COleMessageFilter::BeginBusyState](../vs140/COleMessageFilter--BeginBusyState.md)   
 [COleMessageFilter::SetBusyReply](../vs140/COleMessageFilter--SetBusyReply.md)   
 [COleBusyDialog Class](../vs140/COleBusyDialog-Class.md)