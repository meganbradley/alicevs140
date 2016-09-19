---
title: "LIBRARY"
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
ms.assetid: 1d7ccc92-e088-4ef7-9ef0-25c3862cc051
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LIBRARY
Tells LINK to create a DLL. At the same time, LINK creates an import library, unless an .exp file is used in the build.  
  
```  
LIBRARY [library][BASE=address]  
```  
  
## Remarks  
 The *library* argument specifies the name of the DLL. You can also use the [/OUT](../vs140/-OUT--Output-File-Name-.md) linker option to specify the DLL's output name.  
  
 The BASE=*address* argument sets the base address that the operating system uses to load the DLL. This argument overrides the default DLL location of 0x10000000. See the description of the [/BASE](../Topic/-BASE%20\(Base%20Address\).md) option for details about base addresses.  
  
 Remember to use the [/DLL](../vs140/-DLL--Build-a-DLL-.md) linker option when you build a DLL.  
  
## See Also  
 [Rules for Module-Definition Statements](../vs140/Rules-for-Module-Definition-Statements.md)