---
title: "Casing of namespace name &#39;&lt;namespacename1&gt;&#39; does not match casing of namespace name &#39;&lt;namespacename2&gt;&#39; in file &#39;&lt;filepath&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: adaac2fe-1513-4234-afe7-633a76089f36
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Casing of namespace name &#39;&lt;namespacename1&gt;&#39; does not match casing of namespace name &#39;&lt;namespacename2&gt;&#39; in file &#39;&lt;filepath&gt;&#39;
A namespace appears more than once in the project, but with different casings.  
  
 *Casing* refers to the use of upper-case and lower-case characters in the name of a programming element. Visual Basic is case-insensitive, but the common language runtime (CLR) is case-sensitive. For more information, see "Case Sensitivity in Names" in [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md).  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40055  
  
### To correct this error  
  
-   As a precaution, always use the identical casing in every reference to a namespace. This can prevent misinterpretation by the common language runtime.  
  
## See Also  
 [Namespace Statement](../Topic/Namespace%20Statement.md)   
 [Namespaces in Visual Basic](../Topic/Namespaces%20in%20Visual%20Basic.md)   
 [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md)   
 [Visual Basic Naming Conventions](../Topic/Visual%20Basic%20Naming%20Conventions.md)