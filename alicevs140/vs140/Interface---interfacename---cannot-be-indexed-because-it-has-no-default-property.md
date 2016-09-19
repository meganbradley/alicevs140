---
title: "Interface &#39;&lt;interfacename&gt;&#39; cannot be indexed because it has no default property"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d9d83868-5e81-4ec5-878e-2303489d8f2f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Interface &#39;&lt;interfacename&gt;&#39; cannot be indexed because it has no default property
Index expressions must result in a value whose type is an array, in a value whose type has a set of overloaded default properties, or in a set of overloaded properties. An interface can have only one default method or property. This means that it can either inherit an interface containing a default method or property, or its definition block can contain one method or property that is marked as default.  
  
 **Error ID:** BC30547  
  
### To correct this error  
  
-   Supply a default property in the interface.  
  
## See Also  
 [Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md)