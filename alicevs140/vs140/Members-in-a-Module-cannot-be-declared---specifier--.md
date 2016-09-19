---
title: "Members in a Module cannot be declared &#39;&lt;specifier&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c0560864-64f6-4c76-803f-d9c51df89d62
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Members in a Module cannot be declared &#39;&lt;specifier&gt;&#39;
You have used a specifier that is not valid on a member within a `Module` statement. Modules can never be instantiated, do not support inheritance, and cannot implement interfaces.  
  
 **Error ID:** BC30436  
  
### To correct this error  
  
-   Remove the specifier.  
  
## See Also  
 [Module Statement](../Topic/Module%20Statement.md)