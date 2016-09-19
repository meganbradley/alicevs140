---
title: "Linker Tools Error LNK1140"
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
ms.assetid: 468d7651-a7cd-47b9-aead-5bb2fab56121
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1140
too many modules for program database; link with /PDB:NONE  
  
 The project contains more than 4096 modules.  
  
### To fix by using the following possible solutions  
  
1.  Relink using [/PDB:NONE](../vs140/-PDB--Use-Program-Database-.md).  
  
2.  Compile some modules without debugging information.  
  
3.  Reduce the number of modules.