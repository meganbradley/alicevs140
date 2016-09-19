---
title: "Type argument &#39;&lt;typeargumentname&gt;&#39; does not satisfy the &#39;Structure&#39; constraint for type parameter &#39;&lt;typeparametername&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 09e5a837-8afd-4360-86bd-157e53c47513
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type argument &#39;&lt;typeargumentname&gt;&#39; does not satisfy the &#39;Structure&#39; constraint for type parameter &#39;&lt;typeparametername&gt;&#39;
A type argument supplied to a generic type does not satisfy the value type constraint on its corresponding type parameter.  
  
 A constraint list imposes requirements on the type argument passed to the type parameter. If you do not include any specific class or interface in the constraint list, you can impose a general requirement by specifying one of the following:  
  
-   The type argument must be a value type (include the [Structure (Visual Basic)](assetId:///263ce115-ac36-4c05-8cb7-0e0eead5c6d0) constraint)  
  
-   The type argument must be a reference type (include the [Class (Visual Basic)](assetId:///0777c6e6-46bc-451b-ad70-57b49d4ef4f7) constraint)  
  
 You cannot specify both `Structure` and `Class` for the same type parameter, and you cannot specify either one more than once.  
  
 **Error ID:** BC32105  
  
### To correct this error  
  
-   Select a type argument of any value type.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [How to: Use a Generic Class](../Topic/How%20to:%20Use%20a%20Generic%20Class%20\(Visual%20Basic\).md)