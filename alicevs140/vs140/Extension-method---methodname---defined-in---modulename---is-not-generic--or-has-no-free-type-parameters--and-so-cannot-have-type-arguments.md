---
title: "Extension method &#39;&lt;methodname&gt;&#39; defined in &#39;&lt;modulename&gt;&#39; is not generic (or has no free type parameters) and so cannot have type arguments"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 45191e93-89d1-48ec-99a5-ff9661a2a6ee
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Extension method &#39;&lt;methodname&gt;&#39; defined in &#39;&lt;modulename&gt;&#39; is not generic (or has no free type parameters) and so cannot have type arguments
A type argument has been specified in a call to an extension method that either has no generic parameters or has no generic parameters for which a type is not already specified. For example, the following code causes this error.  
  
```vb#  
' The extension method is not generic.  
<Extension()> _  
Sub Example(ByVal str As String)  
    ' Body of the Sub.  
End Sub  
```  
  
```vb#  
Dim str = "hi"  
'' The call to Example specifies a type argument.  
'' Not valid.  
'str.Example(Of String)()  
```  
  
 **Error ID:** BC36907  
  
### To correct this error  
  
-   Add a type parameter to the extension method definition.  
  
-   Remove the extra type argument from the procedure call.  
  
## See Also  
 [Extension Methods](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)