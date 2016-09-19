---
title: "Exporting Functions from a DLL by Ordinal Rather Than by Name"
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
ms.assetid: 679719fd-d965-4df3-9f7a-7d86ad831702
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Exporting Functions from a DLL by Ordinal Rather Than by Name
The simplest way to export functions from your DLL is to export them by name. This is what happens when you use **__declspec(dllexport)**, for example. But you can instead export functions by ordinal. With this technique, you must use a .def file instead of **__declspec(dllexport)**. To specify a function's ordinal value, append its ordinal to the function name in the .def file. For information about specifying ordinals, see [Exporting from a DLL Using .def Files](../vs140/Exporting-from-a-DLL-Using-DEF-Files.md).  
  
> [!TIP]
>  If you want to optimize your DLL's file size, use the **NONAME** attribute on each exported function. With the **NONAME** attribute, the ordinals are stored in the DLL's export table rather than the function names. This can be a considerable savings if you are exporting many functions.  
  
## What do you want to do?  
  
-   [Use a .def file so I can export by ordinal](../vs140/Exporting-from-a-DLL-Using-DEF-Files.md)  
  
-   [Use __declspec(dllexport)](../vs140/Exporting-from-a-DLL-Using-__declspec-dllexport-.md)  
  
## See Also  
 [Exporting from a DLL](../vs140/Exporting-from-a-DLL.md)