---
title: "&#39;&lt;propertyname&gt;&#39; implicitly defines &#39;&lt;membername&gt;&#39;, which conflicts with a member of the same name in &lt;type&gt; &#39;&lt;typename&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 33d3ca8b-711b-4f76-9b79-d5428b28dd2f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;propertyname&gt;&#39; implicitly defines &#39;&lt;membername&gt;&#39;, which conflicts with a member of the same name in &lt;type&gt; &#39;&lt;typename&gt;&#39;
The name of a type member conflicts with the name of a member implicitly created for a property. Properties implicitly create several implicit variables that can conflict with defined members.  
  
 **Error ID:** BC31060  
  
### To correct this error  
  
-   Rename the explicitly declared member to remove the naming conflict.  
  
## See Also  
 [NOT IN BUILD: How to: Add Fields and Properties to a Class](assetId:///ae53f61b-3abc-413e-8931-703c5f5e8fc2)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [NOT IN BUILD: Properties and Property Procedures](assetId:///23e2a1ec-7e9d-4109-8940-c703d981077b)