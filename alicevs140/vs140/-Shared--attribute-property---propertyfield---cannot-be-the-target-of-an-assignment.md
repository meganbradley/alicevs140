---
title: "&#39;Shared&#39; attribute property &#39;&lt;propertyfield&gt;&#39; cannot be the target of an assignment"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dffa2b07-9609-4aa3-ae58-c0804d8a05d6
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Shared&#39; attribute property &#39;&lt;propertyfield&gt;&#39; cannot be the target of an assignment
An attempt was made to assign a value to a `ReadOnly` or `Shared` property in an attribute.  
  
 **Error ID:** BC31500  
  
### To correct this error  
  
1.  Remove the property assignment statement.  
  
2.  If using properties you developed, remove the `ReadOnly` or `Shared` modifiers from the attribute property.  
  
## See Also  
 [Shared](../Topic/Shared%20\(Visual%20Basic\).md)   
 [NOT IN BUILD: Attributes in Visual Basic](assetId:///620bfc0e-4582-4c8b-8432-ebc5c3dccc22)