---
title: "Exporting C Functions for Use in C or C++ Language Executables"
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
ms.assetid: b51d6e5e-37cf-4c1c-b0bf-fcf188c82f00
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Exporting C Functions for Use in C or C++ Language Executables
If you have functions in a DLL written in C that you want to access from a C language or C++ language module, you should use the **__cplusplus** preprocessor macro to determine which language is being compiled, and then declare these functions with C linkage if being used from a C++ language module. If you use this technique and provide header files for your DLL, these functions can be used by C and C++ users with no change.  
  
 The following code shows a header file that can be used by C and C++ client applications:  
  
```  
// MyCFuncs.h  
#ifdef __cplusplus  
extern "C" {  // only need to export C interface if  
              // used by C++ source code  
#endif  
  
__declspec( dllimport ) void MyCFunc();  
__declspec( dllimport ) void AnotherCFunc();  
  
#ifdef __cplusplus  
}  
#endif  
```  
  
 If you need to link C functions to your C++ executable and the function declaration header files have not used the above technique, in the C++ source file, do the following to prevent the compiler from decorating the C function names:  
  
```  
extern "C" {  
#include "MyCHeader.h"  
}  
```  
  
## What do you want to do?  
  
-   [Export from a DLL using .def files](../vs140/Exporting-from-a-DLL-Using-DEF-Files.md)  
  
-   [Export from a DLL using __declspec(dllexport)](../vs140/Exporting-from-a-DLL-Using-__declspec-dllexport-.md)  
  
-   [Export and import using AFX_EXT_CLASS](../vs140/Exporting-and-Importing-Using-AFX_EXT_CLASS.md)  
  
-   [Determine which exporting method to use](../vs140/Determining-Which-Exporting-Method-to-Use.md)  
  
-   [Import into an application using __declspec(dllimport)](../vs140/Importing-into-an-Application-Using-__declspec-dllimport-.md)  
  
-   [Initialize a DLL](../vs140/Initializing-a-DLL.md)  
  
## What do you want to know more about?  
  
-   [Decorated names](../vs140/Decorated-Names.md)  
  
-   [Linkage specifications](assetId:///d2b0cff1-7798-4c38-9ac8-61c3bfe2bfb9)  
  
## See Also  
 [Exporting from a DLL](../vs140/Exporting-from-a-DLL.md)