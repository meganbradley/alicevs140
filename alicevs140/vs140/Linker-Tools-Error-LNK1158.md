---
title: "Linker Tools Error LNK1158"
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
ms.assetid: 45febf16-d9e1-42db-af91-532e2717fd6a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1158
cannot run 'filename'  
  
 The given executable file called by [LINK](../vs140/Linker-Command-Line-Syntax.md) is not in the directory that contains LINK nor in a directory specified in the PATH environment variable.  
  
 For example, you will get this error if you try to use the PGOPTIMIZE parameter to the [/LTCG](../vs140/-LTCG--Link-time-Code-Generation-.md) linker option on a machine with a 32-bit operating system.