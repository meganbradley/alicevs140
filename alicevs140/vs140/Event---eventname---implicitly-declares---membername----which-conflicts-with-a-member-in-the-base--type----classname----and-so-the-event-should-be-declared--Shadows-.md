---
title: "Event &#39;&lt;eventname&gt;&#39; implicitly declares &#39;&lt;membername&gt;&#39;, which conflicts with a member in the base &lt;type&gt; &#39;&lt;classname&gt;&#39;, and so the event should be declared &#39;Shadows&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5f14e8bd-a227-4115-af99-cd2b6fe4dc0e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event &#39;&lt;eventname&gt;&#39; implicitly declares &#39;&lt;membername&gt;&#39;, which conflicts with a member in the base &lt;type&gt; &#39;&lt;classname&gt;&#39;, and so the event should be declared &#39;Shadows&#39;
An event is declared with a name that combines to form an implicit member with the same name as a member of the base class. For example, if you declare an event named `Event1`, the compiler generates the implicit procedures `add_Event1` and `remove_Event1`. If the base class has a member with one of these names, the event in this class should shadow the base class member.  
  
 This message is a warning. `Shadows` is assumed by default. For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40012  
  
### To correct this error  
  
1.  To hide the base class member, add the `Shadows` keyword to the event declaration.  
  
2.  If you do not intend to hide the base class member, change the name of the event.  
  
## See Also  
 [Event Statement](../vs140/Event-Statement.md)   
 [Shadows](../vs140/Shadows--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)