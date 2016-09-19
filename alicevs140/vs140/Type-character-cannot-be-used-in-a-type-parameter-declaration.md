---
title: "Type character cannot be used in a type parameter declaration"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 24f9a514-f3d4-46c3-805c-71225f6fec59
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type character cannot be used in a type parameter declaration
A type parameter declaration contains at least one identifier type character.  
  
 A type parameter of a generic type must be a valid Visual Basic name. The allowed characters do not include any of the identifier type characters (`%`, `&`, `@`, `!`, `#`, and `$`). See [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md).  
  
 **Error ID:** BC32041  
  
### To correct this error  
  
-   Remove the type identifier character or characters from the type parameter declaration.  
  
## See Also  
 [Type Characters](../vs140/Type-Characters--Visual-Basic-.md)   
 [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)