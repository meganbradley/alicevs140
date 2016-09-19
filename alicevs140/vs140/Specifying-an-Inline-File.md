---
title: "Specifying an Inline File"
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
ms.assetid: 393eccfb-3fc9-4bac-a30c-8ac8d221cca3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specifying an Inline File
Specify two angle brackets (<<) in the command where *filename* is to appear. The angle brackets cannot be a macro expansion.  
  
## Syntax  
  
```  
<<[filename]  
```  
  
## Remarks  
 When the command is run, the angle brackets are replaced by *filename*, if specified, or by a unique NMAKE-generated name. If specified, *filename* must follow angle brackets without a space or tab. A path is permitted. No extension is required or assumed. If *filename* is specified, the file is created in the current or specified directory, overwriting any existing file by that name; otherwise, it is created in the TMP directory (or the current directory, if the TMP environment variable is not defined). If a previous *filename* is reused, NMAKE replaces the previous file.  
  
## See Also  
 [Inline Files in a Makefile](../vs140/Inline-Files-in-a-Makefile.md)