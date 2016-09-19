---
title: "Nullable type inference is not supported in this context"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0a1e2dbc-d9a4-433d-9306-c5540782b81d
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Nullable type inference is not supported in this context
Value types and structures can be declared nullable.  
  
```vb#  
Dim a? As Integer  
Dim b As Integer?  
```  
  
 However, you cannot use the nullable declaration in combination with type inference. The following examples cause this error.  
  
```vb#  
' Not valid.  
' Dim c? = 10  
' Dim d? = a  
```  
  
 **Error ID:** BC36629  
  
### To correct this error  
  
-   Use an `As` clause to declare the variable as nullable.  
  
## See Also  
 [Nullable Value Types](../Topic/Nullable%20Value%20Types%20\(Visual%20Basic\).md)   
 [Local Type Inference](../vs140/Local-Type-Inference--Visual-Basic-.md)