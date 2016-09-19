---
title: "Linkage in Names with Block Scope"
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
ms.assetid: 73efa91a-f761-47f7-bbd9-9f9e3508e218
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linkage in Names with Block Scope
The following linkage rules apply to names with block scope (local names):  
  
-   Names declared as `extern` have external linkage unless they were previously declared as **static**.  
  
-   All other names with block scope have no linkage.  
  
## See Also  
 [Program and Linkage](../vs140/Program-and-Linkage---C---.md)