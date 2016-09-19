---
title: "Compiler Warning (level 4) C4513"
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
ms.assetid: 6877334a-f30a-4184-9483-dac3348737a4
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4513
'class' : destructor could not be generated  
  
 The compiler cannot generate a default destructor for the given class; no destructor was created. The destructor is in a base class that is not accessible to the derived class. If the base class has a private destructor, make it public or protected.