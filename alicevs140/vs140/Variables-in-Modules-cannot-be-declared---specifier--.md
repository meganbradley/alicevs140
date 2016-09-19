---
title: "Variables in Modules cannot be declared &#39;&lt;specifier&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2500b776-7fa4-4272-8cc7-204593706651
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Variables in Modules cannot be declared &#39;&lt;specifier&gt;&#39;
You have used a specifier, such as `MustInherit`, on a variable in a `Module` statement. Modules can never be instantiated, do not support inheritance, and cannot implement interfaces.  
  
 **Error ID:** BC30593  
  
### To correct this error  
  
-   Remove the specifier.  
  
## See Also  
 [Module Statement](../Topic/Module%20Statement.md)