---
title: "Requirements for STL-CLR Container Elements"
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
ms.topic: reference
H1: Requirements for STL/CLR Container Elements
ms.assetid: 59ab240c-15bf-4701-a9f9-e7c56e5ab53f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Requirements for STL-CLR Container Elements
All reference types that are inserted into STL/CLR containers must have, at a minimum, the following elements:  
  
-   A public copy constructor.  
  
-   A public assignment operator.  
  
-   A public destructor.  
  
 Furthermore, associative containers such as [set](../Topic/set%20\(STL-CLR\).md) and [map](../Topic/map%20\(STL-CLR\).md) must have a public comparison operator defined, which is `operator<` by default. Some operations on containers might also require a public default constructor and a public equivalence operator to be defined.  
  
 Like reference types, value types and handles to reference types that are to be inserted into an associative container must have a comparison operator such as `operator<` defined. The requirements for a public copy constructor, public assignment operator, and a public destructor do not exist for value types or handles to reference types.  
  
## See Also  
 [Standard Template Library Conventions](../vs140/Standard-Template-Library.md)