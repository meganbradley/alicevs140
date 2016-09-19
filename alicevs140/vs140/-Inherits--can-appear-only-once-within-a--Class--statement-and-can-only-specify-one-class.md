---
title: "&#39;Inherits&#39; can appear only once within a &#39;Class&#39; statement and can only specify one class"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4ac5b018-5632-4661-8ac6-dbda2f8c4dfe
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Inherits&#39; can appear only once within a &#39;Class&#39; statement and can only specify one class
More than one `Inherits` statement appears in the same class, or an `Inherits` statement specifies more than one class. A class can inherit from only one base class.  
  
 **Error ID:** BC30121  
  
### To correct this error  
  
-   Remove any extra `Inherits` statements and make sure the remaining `Inherits` statement specifies only one base class.  
  
## See Also  
 [Inherits Statement](../vs140/Inherits-Statement.md)   
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)