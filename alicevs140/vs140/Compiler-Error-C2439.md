---
title: "Compiler Error C2439"
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
ms.assetid: 3c5dbe5c-b7d3-4bb0-8619-92f6e280461e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2439
'identifier' : member could not be initialized  
  
 A class, structure, or union member cannot be initialized.  
  
### To fix by checking the following possible causes  
  
1.  Trying to initialize an indirect base class or structure.  
  
2.  Trying to initialize an inherited member of a class or structure. An inherited member must be initialized by the constructor of the class or structure.