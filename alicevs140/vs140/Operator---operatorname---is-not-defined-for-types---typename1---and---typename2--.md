---
title: "Operator &#39;&lt;operatorname&gt;&#39; is not defined for types &#39;&lt;typename1&gt;&#39; and &#39;&lt;typename2&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d2f77450-2bf2-4b1e-b95f-dbc7878f2777
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operator &#39;&lt;operatorname&gt;&#39; is not defined for types &#39;&lt;typename1&gt;&#39; and &#39;&lt;typename2&gt;&#39;
Operator '<operatorname\>' is not defined for types '<typename1\>' and '<typename2\>'. Use 'Is' operator to compare two reference types.  
  
 An attempt was made to use an operator in a way that is inappropriate for the specified types. This error can be caused by using the "=" operator instead of using the `Is` operator to compare two objects.  
  
 **Error ID:** BC31080  
  
### To correct this error  
  
1.  Use `Is` operator to compare two reference types.  
  
2.  Use the `Not` operator in conjunction with the `Is` operator to denote inequality. For example:  
  
     [!CODE [VbVbalrOOP#89](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#89)]  
  
## See Also  
 [Is Operator](../vs140/Is-Operator--Visual-Basic-.md)   
 [= Operator](../vs140/=-Operator--Visual-Basic-.md)   
 [Not Operator](../vs140/Not-Operator--Visual-Basic-.md)