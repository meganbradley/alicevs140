---
title: "Compiler Error C2592"
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
ms.assetid: 833a4d7b-66ef-4d4c-ae83-a533c2b0eb07
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2592
'class': 'base_class_2' is inherited from 'base_class_1' and cannot be re-specified  
  
 You can only specify base classes that do not inherit from other base classes. In this case, only `base_class_1` is needed in the specification of `class` because `base_class_1` already inherits `base_class_2`.