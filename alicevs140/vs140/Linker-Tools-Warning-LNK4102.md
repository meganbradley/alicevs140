---
title: "Linker Tools Warning LNK4102"
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
ms.assetid: bfd1b17e-05c7-4bc2-80d6-2888b1a425b2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4102
export of deleting destructor 'name'; image may not run correctly  
  
 The program has attempted to export a deleting destructor. The resulting delete may occur across a DLL boundary such that a process can free memory that it does not own. Make sure that the given symbol is not listed in your .def file, and that the symbol is not listed as an argument of the **/IMPORT** or **/EXPORT** option in the linker command line.  
  
 If you are rebuilding the C run-time library, you can ignore this message.