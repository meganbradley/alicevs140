---
title: "Linker Tools Error LNK1201"
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
ms.assetid: 64c3f496-a428-4b54-981e-faa82ef9c8a1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1201
error writing to program database 'filename'; check for insufficient disk space, invalid path, or insufficient privilege  
  
 LINK could not write to the program database (PDB) for the output file.  
  
### To fix by checking the following possible causes  
  
1.  File is corrupt. Delete the PDB file and relink.  
  
2.  Not enough disk space to write the file.  
  
3.  Drive is not available, possibly due to a network problem.  
  
4.  The debugger is active on the program you are trying to link.  
  
5.  Out of heap space.  See [C1060](../vs140/Fatal-Error-C1060.md) for more information.