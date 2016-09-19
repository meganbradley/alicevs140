---
title: "Attribute member &#39;&lt;membername&gt;&#39; cannot be the target of an assignment because it is not declared &#39;Public&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f8c958f6-58a4-4aff-b8c3-f2e9481e8132
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Attribute member &#39;&lt;membername&gt;&#39; cannot be the target of an assignment because it is not declared &#39;Public&#39;
An attempt was made to assign a value to a private member of an attribute.  
  
 **Error ID:** BC31511  
  
### To correct this error  
  
1.  Remove the assignment.  
  
2.  If using custom attributes that you developed, change the attribute member's access modifier to `Public`.  
  
## See Also  
 [NOT IN BUILD: Attributes in Visual Basic](assetId:///620bfc0e-4582-4c8b-8432-ebc5c3dccc22)   
 [Public](../vs140/Public--Visual-Basic-.md)