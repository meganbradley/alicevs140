---
title: "COleMessageFilter::Register"
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
ms.assetid: 5eb85e9a-7b22-458e-b335-c7a73078a7f3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleMessageFilter::Register
Registers the message filter with the OLE system DLLs.  
  
## Syntax  
  
```  
  
BOOL Register( );  
  
```  
  
## Return Value  
 Nonzero on success; otherwise 0.  
  
## Remarks  
 A message filter has no effect unless it is registered with the system DLLs. Usually your application's initialization code registers the application's message filter. Any other message filter registered by your application should be revoked before the program terminates by a call to [Revoke](../vs140/COleMessageFilter--Revoke.md).  
  
 The framework's default message filter is automatically registered during initialization and revoked at termination.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleMessageFilter Class](../vs140/COleMessageFilter-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleMessageFilter::Revoke](../vs140/COleMessageFilter--Revoke.md)