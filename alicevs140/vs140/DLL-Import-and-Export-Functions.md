---
title: "DLL Import and Export Functions"
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
ms.assetid: 08d164b9-770a-4e14-afeb-c6f21d9e33e4
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DLL Import and Export Functions
**Microsoft Specific**  
  
 The most complete and up-to-date information on this topic can be found in [dllexport, dllimport](../vs140/dllexport--dllimport.md).  
  
 The **dllimport** and `dllexport` storage-class modifiers are Microsoft-specific extensions to the C language. These modifiers explicitly define the DLL's interface to its client (the executable file or another DLL). Declaring functions as `dllexport` eliminates the need for a module-definition (.DEF) file. You can also use the **dllimport** and `dllexport` modifiers with data and objects.  
  
 The **dllimport** and `dllexport` storage-class modifiers must be used with the extended attribute syntax keyword, `__declspec`, as shown in this example:  
  
```  
#define DllImport   __declspec( dllimport )  
#define DllExport   __declspec( dllexport )  
  
DllExport void func();  
DllExport int i = 10;  
DllExport int j;  
DllExport int n;  
```  
  
 For specific information about the syntax for extended storage-class modifiers, see [Extended Storage-Class Attributes](../vs140/C-Extended-Storage-Class-Attributes.md).  
  
 **END Microsoft Specific**  
  
## See Also  
 [C Function Definitions](../vs140/C-Function-Definitions.md)