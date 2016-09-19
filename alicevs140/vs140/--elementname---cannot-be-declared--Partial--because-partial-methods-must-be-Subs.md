---
title: "&#39;&lt;elementname&gt;&#39; cannot be declared &#39;Partial&#39; because partial methods must be Subs"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 31ca12ab-2c26-4907-a253-e7c57bb4f34b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;elementname&gt;&#39; cannot be declared &#39;Partial&#39; because partial methods must be Subs
Only `Sub` procedures can be declared to be partial methods. For example, the following code causes this error because `partialMethod` is a function.  
  
```  
' Partial Private Function partialMethod(ByVal n As Integer) As Integer  
' End Function  
```  
  
 **Error ID:** BC31437  
  
### To correct this error  
  
-   Convert what you are declaring as a partial method to a `Sub`.  
  
-   Do not use a partial method in this case.  
  
## See Also  
 [Partial Methods](../vs140/Partial-Methods--Visual-Basic-.md)   
 [Sub Procedures](../vs140/Sub-Procedures--Visual-Basic-.md)