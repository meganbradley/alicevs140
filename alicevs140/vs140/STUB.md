---
title: "STUB"
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
ms.assetid: 0a3b9643-19ed-47e9-8173-ee16bc8ed056
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# STUB
When used in a module definition file that builds a virtual device driver (VxD), allows you to specify a file name that contains an IMAGE_DOS_HEADER structure (defined in WINNT.H) to be used in the virtual device driver (VxD), rather than the default header.  
  
```  
STUB:filename  
```  
  
## Remarks  
 An equivalent way to specify *filename* is with the [/STUB](../vs140/-STUB--MS-DOS-Stub-File-Name-.md) linker option.  
  
 STUB is valid in a module definition file only when building a VxD.  
  
## See Also  
 [Rules for Module-Definition Statements](../vs140/Rules-for-Module-Definition-Statements.md)