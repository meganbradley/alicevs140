---
title: "Event &#39;&lt;eventname1&gt;&#39; cannot implement event &#39;&lt;eventname2&gt;&#39; on interface &#39;&lt;interface&gt;&#39; because their delegate types &#39;&lt;delegate1&gt;&#39; and &#39;&lt;delegate2&gt;&#39; do not match"
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
ms.assetid: 2e754b66-5836-48ff-9697-b9c0d7085f18
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event &#39;&lt;eventname1&gt;&#39; cannot implement event &#39;&lt;eventname2&gt;&#39; on interface &#39;&lt;interface&gt;&#39; because their delegate types &#39;&lt;delegate1&gt;&#39; and &#39;&lt;delegate2&gt;&#39; do not match
[!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] cannot implement an event because the delegate type of the event does not match the delegate type of the event in the interface. This error can occur when you define multiple events in an interface and then attempt to implement them together with the same event. An event can implement two or more events only if all implemented events are declared using the `As` syntax and specify the same delegate type.  
  
 **Error ID:** BC31423  
  
### To correct this error  
  
-   Implement the events separately.  
  
     —or—  
  
-   Define the events in the interface using the `As` syntax and specify the same delegate type.  
  
## See Also  
 [Event Statement](../vs140/Event-Statement.md)   
 [Delegate Statement](../vs140/Delegate-Statement.md)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)