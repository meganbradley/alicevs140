---
title: "firstprivate"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db479766-6d3b-4bbd-b28e-b192d826788c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# firstprivate
Specifies that each thread should have its own instance of a variable, and that the variable should be initialized with the value of the variable, because it exists before the parallel construct.  
  
## Syntax  
  
```  
firstprivate(var)  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`var`|The variable to have instances in each thread and that will be initialized with the value of the variable, because it exists before the parallel construct. If more than one variable is specified, separate variable names with a comma.|  
  
## Remarks  
  
## Remarks  
 `firstprivate` applies to the following directives:  
  
-   [for](../vs140/for--OpenMP-.md)  
  
-   [parallel](../vs140/parallel.md)  
  
-   [sections](../vs140/sections--OpenMP-.md)  
  
-   [single](../vs140/single.md)  
  
 For more information, see [2.7.2.2 firstprivate](../vs140/2.7.2.2-firstprivate.md).  
  
## Example  
 For an example of using `firstprivate`, see the example in [private (OpenMP)](../vs140/private--OpenMP-.md).  
  
## See Also  
 [Clauses](../vs140/OpenMP-Clauses.md)