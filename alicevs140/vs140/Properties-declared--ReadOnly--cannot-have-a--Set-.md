---
title: "Properties declared &#39;ReadOnly&#39; cannot have a &#39;Set&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a22eff96-8c18-47c4-9ef0-f98b2ab8a5d8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Properties declared &#39;ReadOnly&#39; cannot have a &#39;Set&#39;
The `Set` procedure writes the value of a property. `ReadOnly` properties cannot be written.  
  
 **Error ID:** BC30022  
  
### To correct this error  
  
-   Remove the `ReadOnly` keyword from the `Property` statement, or remove the `Set` procedure from the property body.  
  
## See Also  
 [Property Statement](../vs140/Property-Statement.md)   
 [Set Statement](../vs140/Set-Statement--Visual-Basic-.md)   
 [ReadOnly](../vs140/ReadOnly--Visual-Basic-.md)