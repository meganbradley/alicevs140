---
title: "Member &#39;&lt;interfacename&gt;.&lt;procedurename&gt;&#39; that matches this signature cannot be implemented because the interface &#39;&lt;interfacename&gt;&#39; contains multiple members with this same name and signature: &lt;signaturelist&gt;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e917d85e-95e0-431a-9d09-39ce5d4fc894
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Member &#39;&lt;interfacename&gt;.&lt;procedurename&gt;&#39; that matches this signature cannot be implemented because the interface &#39;&lt;interfacename&gt;&#39; contains multiple members with this same name and signature: &lt;signaturelist&gt;
A procedure or property attempts to implement a procedure or property defined in an implemented interface, but the compiler finds more than one version of the interface procedure or property with the same name and signature.  
  
 This error can occur in a situation with constructed generic types, as the following skeleton declarations illustrate.  
  
```  
Public Interface baseInterface(Of t)  
    Sub doSomething(ByVal inputValue As String)  
    Sub doSomething(ByVal inputValue As t)  
End Class  
Public Class implementingClass  
    Implements baseInterface(Of String)  
    Sub doSomething(ByVal inputValue As String) _  
        Implements baseInterface(Of String).doSomething  
    End Sub  
End Class  
```  
  
 Because `implementingClass` implements `baseInterface` supplying `String` to its type parameter `t`, the two versions of `doSomething` in `baseInterface` take on identical signatures as far as `implementingClass` is concerned. As a result, the compiler cannot determine which version to implement.  
  
 **Error ID:** BC30937  
  
### To correct this error  
  
-   Change the type argument or arguments you supply to the base class so that it does not result in one or more identical signatures of member procedures or properties.  
  
     -or-  
  
-   Do not implement this base class. You cannot implement it with the set of type arguments you are using, because you must implement every one of its members.  
  
## See Also  
 [Implements (Visual Basic)](../vs140/Implements-Clause--Visual-Basic-.md)   
 [Implements Statement](../vs140/Implements-Statement.md)   
 [NOT IN BUILD: Implements Keyword and Implements Statement](assetId:///b96560f7-6413-480f-a1e2-f80253bab5be)