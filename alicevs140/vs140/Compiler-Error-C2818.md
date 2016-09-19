---
title: "Compiler Error C2818"
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
ms.assetid: 715fc7c9-0c6d-452b-b7f5-1682cea5e907
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2818
application of overloaded 'operator ->' is recursive through type 'type'  
  
 A redefinition of the class member access operator contains a recursive `return` statement. To redefine the `->` operator with recursion, you must move the recursive routine to a separate function called from the operator override function.