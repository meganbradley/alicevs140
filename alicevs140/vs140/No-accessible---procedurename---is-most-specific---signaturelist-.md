---
title: "No accessible &#39;&lt;procedurename&gt;&#39; is most specific: &lt;signaturelist&gt;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 51d54cbb-b530-4661-9952-5ccc17e4220b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# No accessible &#39;&lt;procedurename&gt;&#39; is most specific: &lt;signaturelist&gt;
An assignment statement assigns the address of an overloaded procedure to a delegate variable, but the compiler cannot resolve among the overloaded versions.  
  
 When code uses the address of a procedure that is defined in several overloaded versions, the compiler must decide which of the overloads to use. It tries to find a single version with a parameter list that matches the delegate parameter list. For more information, see [Overload Resolution](../vs140/Overload-Resolution--Visual-Basic-.md).  
  
 If the compiler finds more than one version of the procedure with a matching signature, it generates this error. This can happen, for example, if one of the overloads is generic and a type argument is passed to it that gives it a signature identical to that of another overload.  
  
 **Error ID:** BC30794  
  
### To correct this error  
  
-   If the conflict is caused by a generic overload having the same signature as another overload, change the type argument passed to that generic overload.  
  
## See Also  
 [AddressOf Operator](../vs140/AddressOf-Operator--Visual-Basic-.md)   
 [Delegate Statement](../vs140/Delegate-Statement.md)   
 [NOT IN BUILD: Delegates and the AddressOf Operator](assetId:///7b2ed932-8598-4355-b2f7-5cedb23ee86f)   
 [Overload Resolution](../vs140/Overload-Resolution--Visual-Basic-.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)