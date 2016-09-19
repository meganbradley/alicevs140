---
title: "&#39;AddressOf&#39; expression cannot be converted to &#39;&lt;typename&gt;&#39; because &#39;&lt;typename&gt;&#39; is not a delegate type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5db7589a-5456-4b3a-9d6b-93d9157f0484
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;AddressOf&#39; expression cannot be converted to &#39;&lt;typename&gt;&#39; because &#39;&lt;typename&gt;&#39; is not a delegate type
A statement attempts to convert an `AddressOf` expression to a type that is not a delegate type.  
  
 The `AddressOf` operator creates a procedure delegate instance that references a specific procedure. `AddressOf` can be used as the operand of a delegate constructor, or it can be used in a context in which the type of the delegate can be determined by the compiler.  
  
 **Error ID:** BC30581  
  
### To correct this error  
  
-   Change the target type to a delegate type.  
  
## See Also  
 [AddressOf Operator](../vs140/AddressOf-Operator--Visual-Basic-.md)   
 [NOT IN BUILD: Delegates and the AddressOf Operator](assetId:///7b2ed932-8598-4355-b2f7-5cedb23ee86f)