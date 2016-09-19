---
title: "&#39;}&#39; expected"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a4ce9be9-fc5d-46ec-a217-c3428bd0b97e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;}&#39; expected
An array initializer or a constraint list has not been ended in a valid fashion.  
  
 The element values with which to initialize an array must be enclosed in braces (`{}`).  
  
```  
Dim demoArray() As Integer = New Integer() {1, 2, 3}   
```  
  
 Similarly, the constraints in a constraint list for a generic type parameter must be enclosed in braces.  
  
```  
Public Class dictionaryMaker(Of t As {IComparable, IDisposable, New})   
```  
  
 **Error ID:** BC30370  
  
### To correct this error  
  
-   Use "}" to end the array initializer or constraint list.  
  
## See Also  
 [Arrays](../Topic/Arrays%20in%20Visual%20Basic.md)   
 [How to: Initialize an Array Variable](../vs140/How-to--Initialize-an-Array-Variable-in-Visual-Basic.md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)