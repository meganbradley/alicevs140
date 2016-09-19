---
title: "Template Argument Deduction"
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
ms.assetid: c4aad83b-fc4f-4a20-9603-1939342c6ce1
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Template Argument Deduction
Template arguments are deduced when a call is made to a template function, but some or all template arguments are omitted. The compiler will attempt to deduce the intended template arguments. In most cases, this works as expected. If it does not, a compilation error occurs, in which case you should specify the template arguments explicitly.  
  
 The Visual C++ implementation of template argument deduction conforms to the C++ Standard. For the exact rules on template argument deduction, refer to the ISO Standard.  
  
## See Also  
 [Templates and Name Resolution](../vs140/Templates-and-Name-Resolution.md)