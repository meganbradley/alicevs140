---
title: "Event &#39;&lt;eventname1&gt;&#39; cannot implement event &#39;&lt;eventname2&gt;&#39; because its delegate type does not match the delegate type of another event implemented by &#39;&lt;eventname1&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0b9ffddb-4759-438b-b569-beac7062e986
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event &#39;&lt;eventname1&gt;&#39; cannot implement event &#39;&lt;eventname2&gt;&#39; because its delegate type does not match the delegate type of another event implemented by &#39;&lt;eventname1&gt;&#39;
[!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] cannot implement an event because the delegate type of the event does not match the delegate type of another event. This error can occur when you define multiple events in an interface and then attempt to implement them together with the same event. An event can implement two or more events only if all implemented events are declared using the `As` syntax and specify the same delegate type.  
  
 **Error ID:** BC31407  
  
### To correct this error  
  
-   Implement the events separately.  
  
## See Also  
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)