---
title: "Property without a &#39;ReadOnly&#39; or &#39;WriteOnly&#39; specifier must provide both a &#39;Get&#39; and a &#39;Set&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b24fc997-9a6b-44d1-b712-dab498a6fc72
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property without a &#39;ReadOnly&#39; or &#39;WriteOnly&#39; specifier must provide both a &#39;Get&#39; and a &#39;Set&#39;
If a property is not declared as `ReadOnly` or `WriteOnly`, it must supply procedures for reading and writing its value.  
  
 **Error ID:** BC30124  
  
### To correct this error  
  
1.  Make sure you include both a `Get` procedure and a `Set` procedure between the `Property` statement and the `End Property` statement.  
  
2.  Verify that other procedures within the `Property` declaration are correctly terminated.  
  
## See Also  
 [Property Statement](../vs140/Property-Statement.md)   
 [Get Statement](../vs140/Get-Statement.md)   
 [Set Statement](../vs140/Set-Statement--Visual-Basic-.md)