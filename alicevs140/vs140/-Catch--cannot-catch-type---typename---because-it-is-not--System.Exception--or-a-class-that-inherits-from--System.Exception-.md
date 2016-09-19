---
title: "&#39;Catch&#39; cannot catch type &#39;&lt;typename&gt;&#39; because it is not &#39;System.Exception&#39; or a class that inherits from &#39;System.Exception&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1d513d1d-38f5-4b4e-95bb-9f1209553803
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Catch&#39; cannot catch type &#39;&lt;typename&gt;&#39; because it is not &#39;System.Exception&#39; or a class that inherits from &#39;System.Exception&#39;
`Catch` can only intercept exceptions, and you have attempted to catch something that is not derived from an exception.  
  
 **Error ID:** BC30392  
  
### To correct this error  
  
1.  Remove the `Catch` statement, or change the target of the `Catch` to an actual exception.  
  
## See Also  
 [Try...Catch...Finally Statement](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)   
 [Structured Exception Handling Overview for Visual Basic](assetId:///bb81af80-a735-4873-9711-6151a48e418a)