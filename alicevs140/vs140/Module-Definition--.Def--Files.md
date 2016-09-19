---
title: "Module-Definition (.Def) Files"
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
ms.assetid: 08c0bc28-c5d2-47aa-9624-7fc68bcaa4d8
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module-Definition (.Def) Files
Module-definition (.def) files provide the linker with information about exports, attributes, and other information about the program to be linked. A .def file is most useful when building a DLL. Because there are [linker options](../Topic/Linker%20Options.md) that can be used instead of module-definition statements, .def files are generally not necessary. You can also use [__declspec(dllexport)](../vs140/Exporting-from-a-DLL-Using-__declspec-dllexport-.md) as a way to specify exported functions.  
  
 You can invoke a .def file during the linker phase with the [/DEF (Specify Module-Definition File)](../vs140/-DEF--Specify-Module-Definition-File-.md) linker option.  
  
 If you are building an .exe file that has no exports, using a .def file will make your output file larger and slower loading.  
  
 For an example, see [Exporting from a DLL Using DEF Files](../vs140/Exporting-from-a-DLL-Using-DEF-Files.md).  
  
 See the following sections for more information:  
  
-   [Rules for Module-Definition Statements](../vs140/Rules-for-Module-Definition-Statements.md)  
  
-   [EXPORTS](../vs140/EXPORTS.md)  
  
-   [HEAPSIZE](../vs140/HEAPSIZE.md)  
  
-   [LIBRARY](../vs140/LIBRARY.md)  
  
-   [NAME](../vs140/NAME--C-C---.md)  
  
-   [SECTIONS](../vs140/SECTIONS--C-C---.md)  
  
-   [STACKSIZE](../vs140/STACKSIZE.md)  
  
-   [STUB](../vs140/STUB.md)  
  
-   [VERSION](../vs140/VERSION--C-C---.md)  
  
-   [Reserved words](../vs140/Reserved-Words.md)  
  
## See Also  
 [C/C++ Building Reference](../vs140/C-C---Building-Reference.md)   
 [Linker Options](../Topic/Linker%20Options.md)   
 [Frequently Asked Questions on Building](assetId:///56a3bb8f-0181-4989-bab4-a07ba950ab08)