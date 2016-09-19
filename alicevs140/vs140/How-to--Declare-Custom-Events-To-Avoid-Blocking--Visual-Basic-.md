---
title: "How to: Declare Custom Events To Avoid Blocking (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 998b6a90-67c5-4d2c-8b11-366d3e355505
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Declare Custom Events To Avoid Blocking (Visual Basic)
There are several circumstances when it is important that one event handler not block subsequent event handlers. Custom events allow the event to call its event handlers asynchronously.  
  
 By default, the backing-store field for an event declaration is a multicast delegate that serially combines all the event handlers. This means that if one handler takes a long time to complete, it blocks the other handlers until it completes. (Well-behaved event handlers should never perform lengthy or potentially blocking operations.)  
  
 Instead of using the default implementation of events that Visual Basic provides, you can use a custom event to execute the event handlers asynchronously.  
  
## Example  
 In this example, the `AddHandler` accessor adds the delegate for each handler of the `Click` event to an <xref:System.Collections.ArrayList?qualifyHint=False> stored in the `EventHandlerList` field.  
  
 When code raises the `Click` event, the `RaiseEvent` accessor invokes all the event handler delegates asynchronously using the <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke?qualifyHint=False> method. That method invokes each handler on a worker thread and returns immediately, so handlers cannot block one another.  
  
 [!CODE [VbVbalrEvents#27](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#27)]  
  
## See Also  
 <xref:System.Collections.ArrayList?qualifyHint=False>   
 <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke?qualifyHint=False>   
 [Events (Visual Basic)](../vs140/Events--Visual-Basic-.md)   
 [How to: Declare Events That Conserve Memory Use](../Topic/How%20to:%20Declare%20Custom%20Events%20To%20Conserve%20Memory%20\(Visual%20Basic\).md)