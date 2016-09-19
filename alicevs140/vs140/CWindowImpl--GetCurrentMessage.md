---
title: "CWindowImpl::GetCurrentMessage"
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
ms.assetid: 979a8bf1-4066-4a69-9124-f5545edbb6b6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindowImpl::GetCurrentMessage
Returns the current message, packaged in the `MSG` structure.  
  
## Syntax  
  
```  
  
const MSG* GetCurrentMessage( );  
  
```  
  
## Return Value  
 The current message.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindowImpl Class](../vs140/CWindowImpl-Class.md)   
 [CWindowImpl::OnFinalMessage](../vs140/CWindowImpl--OnFinalMessage.md)   
 [CWindowImpl::UnsubclassWindow](../vs140/CWindowImpl--UnsubclassWindow.md)   
 [CWindowImpl::WindowProc](../vs140/CWindowImpl--WindowProc.md)