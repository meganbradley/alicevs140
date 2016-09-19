---
title: "Type &#39;&lt;typename&gt;&#39; cannot implement interface &#39;&lt;interfacename&gt;&#39; because it declares &#39;&lt;eventsignature&gt;&#39; which has a return type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4f26e71a-949d-4103-b565-35cc8e833d29
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type &#39;&lt;typename&gt;&#39; cannot implement interface &#39;&lt;interfacename&gt;&#39; because it declares &#39;&lt;eventsignature&gt;&#39; which has a return type
A class or structure attempts to implement an interface that declares an event that returns a value.  
  
 Visual Basic does not currently support declaring events that return values.  
  
 **Error ID:** BC30945  
  
### To correct this error  
  
-   Remove the `Implements` statement from the class or structure definition, or implement a different interface.  
  
## See Also  
 [NOT IN BUILD:Events and Event Handlers](assetId:///95074a0d-1cbc-4221-a95a-964185c7f962)   
 [Implements Statement](../vs140/Implements-Statement.md)   
 [NOT IN BUILD: Implements Keyword and Implements Statement](assetId:///b96560f7-6413-480f-a1e2-f80253bab5be)