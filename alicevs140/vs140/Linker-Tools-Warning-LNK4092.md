---
title: "Linker Tools Warning LNK4092"
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
ms.assetid: d569ec47-a338-40e1-940b-8a8061459acb
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4092
shared writable section 'section' contains relocations; image may not run correctly  
  
 The linker emits this warning whenever you have a shared section to warn you of a potentially serious problem.  
  
 One way to share data between multiple processes is to mark a section as "shared." However, marking a section as shared can cause problems. For example, you have a DLL that contains declarations like this in a shared data section:  
  
```  
int var = 1;  
int *pvar = &var;  
```  
  
 The linker cannot resolve `pvar` because its value depends on where the DLL is loaded in memory, so it puts a relocation record in the DLL. When the DLL is loaded into memory, the address of `var` can be resolved and `pvar` assigned. If another process loads the same DLL but cannot load it at the same address, the relocation for the address of `var` will be updated for the second process and the first process's address space will point to the wrong address.