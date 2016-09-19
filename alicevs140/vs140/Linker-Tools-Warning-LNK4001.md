---
title: "Linker Tools Warning LNK4001"
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
ms.assetid: 0a8b1c3a-64ce-4311-b7c0-065995059246
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4001
no object files specified; libraries used  
  
 The linker was passed one or more .lib files, but no .obj files.  
  
 Because the linker is not able to access information in a .lib file that it is able to access in an .obj file, this warning indicates that you will have to explicitly specify other linker options. For example, you may have to specify the [/MACHINE](../Topic/-MACHINE%20\(Specify%20Target%20Platform\).md), [/OUT](../vs140/-OUT--Output-File-Name-.md), or [/ENTRY](../vs140/-ENTRY--Entry-Point-Symbol-.md) options.