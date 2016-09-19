---
title: "Anonymous type member name must be preceded by a period"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b87be29e-39f0-4830-9969-608d71137e3e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Anonymous type member name must be preceded by a period
In the object initializer list for an anonymous type declaration, a new member name to which a value is assigned must be preceded by a period. The following example shows a valid and an invalid declaration:  
  
```vb#  
' Valid.  
Dim instanceName1 = New With {.memberName = 10}  
' Invalid declaration that causes this error.  
' Dim instanceName2 = New With {memberName = 10}  
```  
  
 **Error ID:** BC36575  
  
### To correct this error  
  
-   Add a period before the member name.  
  
## See Also  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)