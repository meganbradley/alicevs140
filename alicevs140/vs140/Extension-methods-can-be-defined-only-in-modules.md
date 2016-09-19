---
title: "Extension methods can be defined only in modules"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c832d523-5bf6-4baf-b91c-bd26d94453ed
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Extension methods can be defined only in modules
This error occurs when an extension method has been defined outside a module. In Visual Basic, all extension methods must be defined within standard modules.  
  
 **Error ID:** BC36551  
  
### To correct this error  
  
-   Place the extension method in a module.  
  
## Example  
 The following example extends the `String` class, adding a `Print` method.  
  
```  
Imports StringUtility  
Imports System.Runtime.CompilerServices  
Namespace StringUtility  
    <Extension()> _  
    Module StringExtensions  
        <Extension()> _  
        Public Sub Print (ByVal str As String)  
            Console.WriteLine(str)  
        End Sub  
    End Module  
End Namespace  
```  
  
## See Also  
 [NOT IN BUILD: Application of Attributes](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [Extension Methods (Visual Basic)](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Module (Visual Basic)](../vs140/Module--keyword---Visual-Basic-.md)   
 [Module Statement](../Topic/Module%20Statement.md)