---
title: "Linker Tools Error LNK2027"
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
ms.assetid: e2f857a8-8e8a-4697-bbff-12ccb84a35c1
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK2027
unresolved module reference 'module'  
  
 A file passed to the linker has a dependency on a module that was neither specified with **/ASSEMBLYMODULE** nor passed directly to the linker.  
  
 To resolve LNK2027, do one of the following:  
  
-   Do not pass to the linker the file that has the module dependency.  
  
-   Specify the module with **/ASSEMBLYMODULE**.  
  
-   If the module is a safe .netmodule, pass the module directly to the linker.  
  
 For more information, see [/ASSEMBLYMODULE (Add a MSIL Module to the Assembly)](../Topic/-ASSEMBLYMODULE%20\(Add%20a%20MSIL%20Module%20to%20the%20Assembly\).md) and [.netmodule Files as Linker Input](../vs140/.netmodule-Files-as-Linker-Input.md).