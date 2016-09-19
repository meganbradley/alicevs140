---
title: "Linkage in Names with File Scope"
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
ms.topic: language-reference
ms.assetid: 38d3fa5e-1861-466e-a590-84b86f7b184e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linkage in Names with File Scope
The following linkage rules apply to names (other than `typedef` and enumerator names) with file scope:  
  
-   If a name is explicitly declared as **static**, it has internal linkage and identifies a program element inside its own translation unit.  
  
-   Enumerator names and `typedef` names have no linkage.  
  
-   All other names with file scope have external linkage.  
  
 **Microsoft Specific**  
  
-   If a function name with file scope is explicitly declared as **inline**, it has external linkage if it is instantiated or its address is referenced. Therefore, it is possible for a function with file scope to have either internal or external linkage.  
  
 **END Microsoft Specific**  
  
 A class has internal linkage if it:  
  
-   Uses no C++ functionality (for example, member-access control, member functions, constructors, destructors, and so on).  
  
-   Is not used in the declaration of another name that has external linkage. This constraint means that objects of class type that are passed to functions with external linkage cause the class to have external linkage.  
  
## See Also  
 [Program and Linkage](../vs140/Program-and-Linkage---C---.md)