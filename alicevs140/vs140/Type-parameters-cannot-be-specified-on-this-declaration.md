---
title: "Type parameters cannot be specified on this declaration"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 94cfe3de-74fd-4a2c-9246-ec4a05b73d55
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type parameters cannot be specified on this declaration
A programming element is declared with a type parameter list, but the programming element is not eligible to be a generic type.  
  
 Programming elements that are not eligible to be generic include properties, operators, events, and constructors. Declaring any of these elements with a type parameter list results in this error.  
  
 **Error ID:** BC32065  
  
### To correct this error  
  
-   Remove the `Of` keyword and the type parameters from the declaration.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)