---
title: "Resource Compiler Fatal Error RC1120"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 4e462931-e42e-42e3-8bfc-847677194286
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Resource Compiler Fatal Error RC1120
out of memory, needed number bytes  
  
 The Resource Compiler ran out of storage for items that it stores in its heap. Usually this is the result of having too many symbols.  
  
### To fix by using the following possible solutions  
  
1.  Increase the Windows swap file space. For more information about increasing the swap-file space, see virtual memory in Windows help.  
  
2.  Eliminate unnecessary include files, especially unneeded `#define`s and function prototypes.  
  
3.  Split the current file into two or more files and compile them separately.  
  
4.  Remove other programs or drivers running in the system, which could be consuming significant amounts of memory.