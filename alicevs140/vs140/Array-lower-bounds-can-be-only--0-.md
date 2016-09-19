---
title: "Array lower bounds can be only &#39;0&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 273b69df-910e-45d2-acac-632005d24c5a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array lower bounds can be only &#39;0&#39;
A declaration statement or `New` clause specifies an array with a lower bound other than 0.  
  
 When you create or initialize an array variable, you can optionally specify the upper bound of each dimension. If you do, the length of that dimension becomes the upper bound plus one, because the lower bound is always zero. You can optionally specify the lower bound as well, but you must specify 0. The advantage of doing so is that your code is easier to read.  
  
 **Error ID:** BC32059  
  
### To correct this error  
  
-   Change the lower bound specification to 0, or remove it entirely.  
  
## See Also  
 [Arrays in Visual Basic](../Topic/Arrays%20in%20Visual%20Basic.md)   
 [NOTINBUILD How to: Specify a Zero Lower Bound on an Array](assetId:///20ffd49a-64f7-4634-8ed0-46ba1049d935)