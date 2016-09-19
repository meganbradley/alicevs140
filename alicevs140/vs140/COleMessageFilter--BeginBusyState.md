---
title: "COleMessageFilter::BeginBusyState"
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
ms.assetid: 7d46af56-4911-440b-8282-e3016436d108
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleMessageFilter::BeginBusyState
Call this function to begin a busy state.  
  
## Syntax  
  
```  
  
virtual void BeginBusyState( );  
```  
  
## Remarks  
 It works in conjunction with [EndBusyState](../vs140/COleMessageFilter--EndBusyState.md) to control the application's busy state. The function [SetBusyReply](../vs140/COleMessageFilter--SetBusyReply.md) determines the application's reply to calling applications when it is busy.  
  
 The `BeginBusyState` and `EndBusyState` calls increment and decrement, respectively, a counter that determines whether the application is busy. For example, two calls to `BeginBusyState` and one call to `EndBusyState` still result in a busy state. To cancel a busy state it is necessary to call `EndBusyState` the same number of times `BeginBusyState` has been called.  
  
 By default, the framework enters the busy state during idle processing, which is performed by [CWinApp::OnIdle](../vs140/CWinApp--OnIdle.md). While the application is handling **ON_COMMANDUPDATEUI** notifications, incoming calls are handled later, after idle processing is complete.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleMessageFilter Class](../vs140/COleMessageFilter-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleMessageFilter::EndBusyState](../vs140/COleMessageFilter--EndBusyState.md)   
 [COleMessageFilter::SetBusyReply](../vs140/COleMessageFilter--SetBusyReply.md)   
 [CWinApp::OnIdle](../vs140/CWinApp--OnIdle.md)