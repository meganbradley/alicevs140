---
title: "main Function Restrictions"
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
ms.assetid: 7b3df731-344b-44a8-850c-11cbcbfbfa83
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# main Function Restrictions
Several restrictions apply to the **main** function that do not apply to any other C++ functions. The **main** function:  
  
-   Cannot be overloaded (see [Overloading](../vs140/Overloading---C---.md)).  
  
-   Cannot be declared as **inline**.  
  
-   Cannot be declared as **static**.  
  
-   Cannot have its address taken.  
  
-   Cannot be called.  
  
## See Also  
 [main: Program Startup](../vs140/main--Program-Startup.md)