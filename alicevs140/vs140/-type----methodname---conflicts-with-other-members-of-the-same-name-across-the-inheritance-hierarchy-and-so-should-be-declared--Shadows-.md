---
title: "&lt;type&gt; &#39;&lt;methodname&gt;&#39; conflicts with other members of the same name across the inheritance hierarchy and so should be declared &#39;Shadows&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3081635f-99a9-4e90-997f-82251144d80f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;type&gt; &#39;&lt;methodname&gt;&#39; conflicts with other members of the same name across the inheritance hierarchy and so should be declared &#39;Shadows&#39;
An interface inheriting from two or more interfaces defines a procedure with the same name as a procedure already defined in more than one of the base interfaces. The procedure in this interface should shadow one of the base interface procedures.  
  
 This message is a warning. `Shadows` is assumed by default. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42000  
  
### To correct this error  
  
-   If you intend to hide one of the base interface procedures, add the `Shadows` keyword to the new procedure declaration.  
  
-   If you do not intend to hide any of the base interface procedures, change the name of the new procedure.  
  
## See Also  
 [Shadows](../vs140/Shadows--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)