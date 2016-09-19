---
title: "Enum types cannot be nullable"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9e0fe5c9-72c7-4905-b177-d00cc3469ea9
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Enum types cannot be nullable
The underlying type that is used to declare an enumeration cannot be nullable. For example, the following code causes this error:  
  
```vb#  
'' Not valid.  
' Enum exampleEnum As Integer?  
'     Member declarations.  
' End Enum  
```  
  
 **Error ID:** BC32129  
  
### To correct this error  
  
-   Do not use a nullable underlying type in an `Enum` declaration.  
  
## See Also  
 [Nullable Value Types](../Topic/Nullable%20Value%20Types%20\(Visual%20Basic\).md)   
 [Enum Statement](../Topic/Enum%20Statement%20\(Visual%20Basic\).md)