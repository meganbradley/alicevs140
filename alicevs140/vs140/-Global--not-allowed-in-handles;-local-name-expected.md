---
title: "&#39;Global&#39; not allowed in handles; local name expected"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7b4602a9-84c9-4068-81bc-e8df03ffc130
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Global&#39; not allowed in handles; local name expected
A `Handles` clause must refer to a local event. The `Global` keyword provides access to global programming elements.  
  
 **Error ID:** BC36002  
  
### To correct this error  
  
-   Change the `Handles` clause to refer to a local instance of the event instead of the global instance.  
  
## See Also  
 [Global - delete](assetId:///18c8ba14-40f6-4978-8096-6a5852324635)   
 [Handles](../vs140/Handles-Clause--Visual-Basic-.md)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)