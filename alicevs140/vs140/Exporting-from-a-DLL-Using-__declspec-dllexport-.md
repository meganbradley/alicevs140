---
title: "Exporting from a DLL Using __declspec(dllexport)"
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
ms.assetid: a35e25e8-7263-4a04-bad4-00b284458679
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Exporting from a DLL Using __declspec(dllexport)
Microsoft introduced **__export** in the 16-bit compiler version of Visual C++ to allow the compiler to generate the export names automatically and place them in a .lib file. This .lib file can then be used just like a static .lib to link with a DLL.  
  
 In newer compiler versions, you can export data, functions, classes, or class member functions from a DLL using the **__declspec(dllexport)** keyword. **__declspec(dllexport)** adds the export directive to the object file so you do not need to use a .def file.  
  
 This convenience is most apparent when trying to export decorated C++ function names. Because there is no standard specification for name decoration, the name of an exported function might change between compiler versions. If you use **__declspec(dllexport)**, recompiling the DLL and dependent .exe files is necessary only to account for any naming convention changes.  
  
 Many export directives, such as ordinals, NONAME, and PRIVATE, can be made only in a .def file, and there is no way to specify these attributes without a .def file. However, using **__declspec(dllexport)** in addition to using a .def file does not cause build errors.  
  
 To export functions, the **__declspec(dllexport)** keyword must appear to the left of the calling-convention keyword, if a keyword is specified. For example:  
  
```  
__declspec(dllexport) void __cdecl Function1(void);  
```  
  
 To export all of the public data members and member functions in a class, the keyword must appear to the left of the class name as follows:  
  
```  
class __declspec(dllexport) CExampleExport : public CObject  
{ ... class definition ... };  
```  
  
> [!NOTE]
>  `__declspec(dllexport)` cannot be applied to a function with the `__clrcall` calling convention.  
  
 When building your DLL, you typically create a header file that contains the function prototypes and/or classes you are exporting and add **__declspec(dllexport)** to the declarations in the header file. To make your code more readable, define a macro for **__declspec(dllexport)** and use the macro with each symbol you are exporting:  
  
```  
#define DllExport   __declspec( dllexport )   
```  
  
 **__declspec(dllexport)** stores function names in the DLL's export table. If you want to optimize the table's size, see [Exporting Functions from a DLL by Ordinal Rather Than by Name](../vs140/Exporting-Functions-from-a-DLL-by-Ordinal-Rather-Than-by-Name.md).  
  
> [!NOTE]
>  When porting DLL source code from Win16 to Win32, replace each instance of **__export** with **__declspec(dllexport)**.  
  
 As a reference, search through the Win32 Winbase.h header file. It contains examples of **__declspec(dllimport)** usage.  
  
## What do you want to do?  
  
-   [Export from a DLL using .def files](../vs140/Exporting-from-a-DLL-Using-DEF-Files.md)  
  
-   [Export and import using AFX_EXT_CLASS](../vs140/Exporting-and-Importing-Using-AFX_EXT_CLASS.md)  
  
-   [Export C++ functions for use in C-language executables](../vs140/Exporting-C---Functions-for-Use-in-C-Language-Executables.md)  
  
-   [Export C functions for use in C or C++-language executables](../vs140/Exporting-C-Functions-for-Use-in-C-or-C---Language-Executables.md)  
  
-   [Determine which exporting method to use](../vs140/Determining-Which-Exporting-Method-to-Use.md)  
  
-   [Import into an application using __declspec(dllimport)](../vs140/Importing-into-an-Application-Using-__declspec-dllimport-.md)  
  
-   [Initialize a DLL](../vs140/Initializing-a-DLL.md)  
  
## What do you want to know more about?  
  
-   [The __declspec keyword](../vs140/__declspec.md)  
  
-   [Importing and exporting inline functions](../vs140/Importing-and-Exporting-Inline-Functions.md)  
  
-   [Mutual imports](../vs140/Mutual-Imports.md)  
  
## See Also  
 [Exporting from a DLL](../vs140/Exporting-from-a-DLL.md)