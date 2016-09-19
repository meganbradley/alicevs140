---
title: "&#39;&lt;derivedtypename&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;constructedbasetypename&gt;&#39; because it expands the access of type &#39;&lt;internaltypename&gt;&#39; outside the assembly"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 81909654-7e67-4b89-81a3-25ae57f678f7
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;derivedtypename&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;constructedbasetypename&gt;&#39; because it expands the access of type &#39;&lt;internaltypename&gt;&#39; outside the assembly
A derived class or interface attempts to expand the access level of a restricted type by using it as a type argument to a base class or interface.  
  
 The following code can generate this error.  
  
```  
Public Class baseClass(Of t)  
End Class  
Public Class derivedClass  
    Inherits baseClass(Of restrictedStructure)  
End Class  
Friend Structure restrictedStructure  
    Dim firstMember As Integer  
End Structure  
```  
  
 Code outside the assembly is not allowed to access `restrictedStructure`. However, `derivedClass` can be accessed from any code that can reference it. Therefore, `derivedClass` cannot inherit `baseClass` if it uses `restrictedStructure` as a type argument, because that could expose `restrictedStructure` to code in any assembly.  
  
 **Error ID:** BC30922  
  
### To correct this error  
  
-   Adjust the access levels of the classes or interfaces so the derived type does not expand the access level of the restricted type.  
  
     -or-  
  
-   If you cannot adjust the access levels, do not use the restricted type as a type argument when constructing the base class or interface.  
  
## See Also  
 [Inherits Statement](../vs140/Inherits-Statement.md)   
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)   
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)