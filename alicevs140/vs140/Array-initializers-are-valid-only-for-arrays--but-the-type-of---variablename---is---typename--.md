---
title: "Array initializers are valid only for arrays, but the type of &#39;&lt;variablename&gt;&#39; is &#39;&lt;typename&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3cf34882-7a58-4074-8ebb-52e58199a506
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array initializers are valid only for arrays, but the type of &#39;&lt;variablename&gt;&#39; is &#39;&lt;typename&gt;&#39;
An attempt was made to initialize a non-array variable with a list of values.  
  
 **Error ID:** BC30679  
  
### To correct this error  
  
-   Declare and initialize the variable as an array; for example:  
  
     `Dim intarray As Integer() = {1, 5, 9}`  
  
-   Initialize the variable as a single value; for example:  
  
     `Dim intvalue As Integer = 1`  
  
## See Also  
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [Variable Declaration](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)   
 [Arrays](../Topic/Arrays%20in%20Visual%20Basic.md)