---
title: "NAME (C-C++)"
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
H1: NAME (C/C++)
ms.assetid: 5c9b6bd8-9275-46a5-afba-f17a5936dc26
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NAME (C-C++)
Specifies a name for the main output file.  
  
```  
NAME [application][BASE=address]  
```  
  
## Remarks  
 An equivalent way to specify an output file name is with the [/OUT](../vs140/-OUT--Output-File-Name-.md) linker option, and an equivalent way to set the base address is with the [/BASE](../Topic/-BASE%20\(Base%20Address\).md) linker option. If both are specified, /OUT overrides **NAME**.  
  
 If you build a DLL, NAME will only affect the DLL name.  
  
## See Also  
 [Rules for Module-Definition Statements](../vs140/Rules-for-Module-Definition-Statements.md)