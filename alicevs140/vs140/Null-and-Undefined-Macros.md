---
title: "Null and Undefined Macros"
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
ms.topic: article
ms.assetid: 1db4611a-1755-4328-b00f-d35365af8b6c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Null and Undefined Macros
Both null and undefined macros expand to null strings, but a macro defined as a null string is considered defined in preprocessing expressions. To define a macro as a null string, specify no characters except spaces or tabs after the equal sign (=) in a command line or command file, and enclose the null string or definition in double quotation marks (" "). To undefine a macro, use **!UNDEF.** For more information, see [Makefile Preprocessing Directives](../vs140/Makefile-Preprocessing-Directives.md).  
  
## See Also  
 [Defining an NMAKE Macro](../vs140/Defining-an-NMAKE-Macro.md)