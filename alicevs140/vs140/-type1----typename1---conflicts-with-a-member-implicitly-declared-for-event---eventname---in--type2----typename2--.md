---
title: "&lt;type1&gt; &#39;&lt;typename1&gt;&#39; conflicts with a member implicitly declared for event &#39;&lt;eventname&gt;&#39; in &lt;type2&gt; &#39;&lt;typename2&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de5b1121-8c8f-4aba-a3e7-1e3e60df0dc5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;type1&gt; &#39;&lt;typename1&gt;&#39; conflicts with a member implicitly declared for event &#39;&lt;eventname&gt;&#39; in &lt;type2&gt; &#39;&lt;typename2&gt;&#39;
The name of a type member conflicts with the name of a member implicitly created for an event. Events implicitly create several implicit variables. For example, the declaration `Event X` implicitly declares the names `XEventHandler`, `XEvent`, `add_X`, and `remove_X`.  
  
 **Error ID:** BC31061  
  
### To correct this error  
  
-   Rename the explicitly declared member to remove the naming conflict.  
  
## See Also  
 [NotInBuild:Declaration Statements in Visual Basic](assetId:///81f3c398-f45c-4d95-80bf-aa39d1a0fb30)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)