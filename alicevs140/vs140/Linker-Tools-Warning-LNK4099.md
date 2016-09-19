---
title: "Linker Tools Warning LNK4099"
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
ms.assetid: 358170a4-07cd-43fe-918f-82c32757ffc5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4099
PDB 'filename' was not found with 'object/library' or at 'path'; linking object as if no debug info  
  
 The linker was unable to find your .pdb file. Copy it into the directory that contains `object/library`.  
  
 To find the name of the .pdb file associated with the object file:  
  
1.  Extract an object file from the library with [lib](../vs140/LIB-Reference.md) **/extract:**`objectname`**.obj** `xyz`**.lib**.  
  
2.  Check the path to the .pdb file with **dumpbin /section:.debug$T /rawdata** `objectname`**.obj**.  
  
 You could also compile with [/Z7](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md), so the pdb doesn't need to be used, or remove the [/DEBUG](../Topic/-DEBUG%20\(Generate%20Debug%20Info\).md) linker option if you do not have .pdb files for the objects you are linking.