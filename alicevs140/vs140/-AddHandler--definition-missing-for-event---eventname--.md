---
title: "&#39;AddHandler&#39; definition missing for event &#39;&lt;eventname&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cf6c7fd6-ce2e-4916-b427-2a4a63e7279d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;AddHandler&#39; definition missing for event &#39;&lt;eventname&gt;&#39;
If an event is declared as `Custom`, it must supply a procedure for adding an event handler.  
  
 **Error ID:** BC31130  
  
### To correct this error  
  
1.  Include an `AddHandler` declaration between the `Custom Event` statement and the `End Event` statement.  
  
2.  Verify that other procedures within the event declaration end correctly.  
  
## See Also  
 [AddHandler Statement](../vs140/AddHandler-Statement.md)   
 [Event Statement](../vs140/Event-Statement.md)