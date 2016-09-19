---
title: "Compiler Error C2170"
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
ms.assetid: d5c663f0-2459-4e11-a8bf-a52b62f3c71d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2170
'identifier' : not declared as a function, cannot be intrinsic  
  
### To fix by checking the following possible causes  
  
1.  Pragma `intrinsic` is used for an item other than a function.  
  
2.  Pragma `intrinsic` is used for a function with no intrinsic form.