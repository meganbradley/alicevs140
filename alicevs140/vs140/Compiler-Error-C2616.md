---
title: "Compiler Error C2616"
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
ms.assetid: 8d0c02d6-a0b0-4135-b10f-438d67da68c6
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2616
'conversion' : cannot implicitly convert a non-lvalue 'type1' to a 'type2' that is not const  
  
 A reference cannot be initialized from a non-lvalue.  
  
 This is an error under ANSI compatibility ([/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)) and a warning under Microsoft extensions (**/Ze**).