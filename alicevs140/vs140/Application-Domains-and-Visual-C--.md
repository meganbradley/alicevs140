---
title: "Application Domains and Visual C++"
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
ms.assetid: 75a08efc-9b02-40ba-99b7-dcbd71010bbf
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Application Domains and Visual C++
If you have a `__clrcall` virtual function, the vtable will be per application domain (appdomain). If you create an object in one appdomain, you can only call the virtual function from within that appdomain. All functions defined in **/clr:pure** compilands use the `__clrcall` calling convention. Therefore, all vtables defined in **/clr:pure** compilands are per appdomain. In mixed mode (**/clr**) you will have per process vtables if your type has no `__clrcall` virtual functions.  
  
 For more information, see  
  
-   [appdomain](../vs140/appdomain.md)  
  
-   [__clrcall](../Topic/__clrcall.md)  
  
-   [How to: Migrate to /clr:pure](../vs140/How-to--Migrate-to--clr-pure--C---CLI-.md)  
  
-   [process](../vs140/process.md)  
  
## See Also  
 [Mixed Assemblies](../vs140/Mixed--Native-and-Managed--Assemblies.md)