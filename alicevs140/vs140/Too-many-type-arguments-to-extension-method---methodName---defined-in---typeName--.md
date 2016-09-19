---
title: "Too many type arguments to extension method &#39;&lt;methodName&gt;&#39; defined in &#39;&lt;typeName&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 504c9b1f-f511-4198-8970-136d1a1bdafe
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Too many type arguments to extension method &#39;&lt;methodName&gt;&#39; defined in &#39;&lt;typeName&gt;&#39;
A generic extension method has been invoked with more type arguments than there are type parameters.  
  
 When you invoke a generic method, you must supply one type argument for each type parameter defined by that method.  
  
 **Error ID:** BC36591  
  
### To correct this error  
  
-   Remove type arguments from your type argument list so that there is one for each type parameter defined by the generic method that you are invoking.  
  
## See Also  
 [Extension Methods (Visual Basic)](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)