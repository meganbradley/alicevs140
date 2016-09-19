---
title: "Compiler Error C2873"
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
ms.topic: error-reference
ms.assetid: 7a10036b-400e-4364-bd2f-dcd7370c5e28
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2873
'symbol' : symbol cannot be used in a using-declaration  
  
 A `using` directive is missing a [namespace](../vs140/namespace-Declaration.md) keyword. This causes the compiler to misinterpret the code as a [using declaration](../vs140/using-Declaration.md) rather than a [using directive](../vs140/using-Directive--C---.md).