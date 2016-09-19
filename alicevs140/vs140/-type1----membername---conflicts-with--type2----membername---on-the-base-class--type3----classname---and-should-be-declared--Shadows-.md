---
title: "&lt;type1&gt; &#39;&lt;membername&gt;&#39; conflicts with &lt;type2&gt; &#39;&lt;membername&gt;&#39; on the base class &lt;type3&gt; &#39;&lt;classname&gt;&#39; and should be declared &#39;Shadows&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 24d10f31-3b3d-448c-b928-fc937e1f4a92
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;type1&gt; &#39;&lt;membername&gt;&#39; conflicts with &lt;type2&gt; &#39;&lt;membername&gt;&#39; on the base class &lt;type3&gt; &#39;&lt;classname&gt;&#39; and should be declared &#39;Shadows&#39;
A programming element is declared with the same name as an element defined in the base class. In this situation, the element in this class should shadow the base class element.  
  
 This message is a warning. `Shadows` is assumed by default. For more information about hiding warnings or treating warnings as errors, please see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40004  
  
### To correct this error  
  
-   Add the `Shadows` keyword to the declaration, or change the name of the element being declared.  
  
## See Also  
 [Shadows](../vs140/Shadows--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)