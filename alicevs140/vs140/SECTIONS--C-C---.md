---
title: "SECTIONS (C-C++)"
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
H1: SECTIONS (C/C++)
ms.assetid: 7b974366-9ef5-4e57-bbcc-73a1df6f8857
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SECTIONS (C-C++)
Introduces a section of one or more `definitions` that are access specifiers on sections in your project's output file.  
  
```  
SECTIONS  
definitions  
```  
  
## Remarks  
 Each definition must be on a separate line. The `SECTIONS` keyword can be on the same line as the first definition or on a preceding line. The .def file can contain one or more `SECTIONS` statements.  
  
 This `SECTIONS` statement sets attributes for one or more sections in the image file, and can be used to override the default attributes for each type of section.  
  
 The format for `definitions` is:  
  
 `.section_name specifier`  
  
 where `.section_name` is the name of a section in your program image and `specifier`is one or more of the following access modifiers:  
  
|Modifier|Description|  
|--------------|-----------------|  
|`EXECUTE`|The section is executable|  
|`READ`|Allows read operations on data|  
|`SHARED`|Shares the section among all processes that load the image|  
|`WRITE`|Allows write operations on data|  
  
 Separate specifier names with a space. For example:  
  
```  
SECTIONS  
.rdata READ WRITE  
```  
  
 `SECTIONS` marks the beginning of a list of section `definitions`. Each `definition` must be on a separate line. The `SECTIONS` keyword can be on the same line as the first `definition` or on a preceding line. The .def file can contain one or more `SECTIONS` statements. The `SEGMENTS` keyword is supported as a synonym for `SECTIONS`.  
  
 Older versions of Visual C++ supported:  
  
```  
section [CLASS 'classname'] specifier  
```  
  
 The `CLASS` keyword is supported for compatibility, but is ignored.  
  
 An equivalent way to specify section attributes is with the [/SECTION](../vs140/-SECTION--Specify-Section-Attributes-.md) option.  
  
## See Also  
 [Rules for Module-Definition Statements](../vs140/Rules-for-Module-Definition-Statements.md)