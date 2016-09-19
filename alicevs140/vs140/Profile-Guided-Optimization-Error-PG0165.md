---
title: "Profile-Guided Optimization Error PG0165"
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
ms.assetid: e98122e7-ddee-4a2c-96b2-d232e4c65f3e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Profile-Guided Optimization Error PG0165
Reading 'Filename.pgd' : 'PGD version is not supported (version mismatch)'.  
  
 PGD files are specific to a particular compiler toolset. This error is generated when you are using a different compiler than the one used for *Filename*.pgd. This error indicates that this compiler toolset cannot use the data from *Filename*.pgd to optimize the current program.  
  
 To resolve this problem, regenerate *Filename*.pgd by using the current compiler toolset.