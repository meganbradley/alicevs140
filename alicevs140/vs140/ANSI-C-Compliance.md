---
title: "ANSI C Compliance"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6be271bf-eecf-491a-a928-0ee2dd60e3b9
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ANSI C Compliance
The naming convention for all Microsoft-specific identifiers in the run-time system (such as functions, macros, constants, variables, and type definitions) is ANSI-compliant. In this documentation, any run-time function that follows the ANSI/ISO C standards is noted as being ANSI compatible. ANSI-compliant applications should only use these ANSI compatible functions.  
  
 The names of Microsoft-specific functions and global variables begin with a single underscore. These names can be overridden only locally, within the scope of your code. For example, when you include Microsoft run-time header files, you can still locally override the Microsoft-specific function named `_open` by declaring a local variable of the same name. However, you cannot use this name for your own global function or global variable.  
  
 The names of Microsoft-specific macros and manifest constants begin with two underscores, or with a single leading underscore immediately followed by an uppercase letter. The scope of these identifiers is absolute. For example, you cannot use the Microsoft-specific identifier **_UPPER** for this reason.  
  
## See Also  
 [Compatibility](../vs140/Compatibility.md)