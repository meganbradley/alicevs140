---
title: "Explicitly Unloading a Delay-Loaded DLL"
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
ms.assetid: 1c4c5172-fd06-45d3-9e4f-f12343176b3c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Explicitly Unloading a Delay-Loaded DLL
The [/delay](../vs140/-DELAY--Delay-Load-Import-Settings-.md):unload linker option allows you to unload a DLL that was delay loaded. By default, when your code unloads the DLL (using /delay:unload and **__FUnloadDelayLoadedDLL2**), the delay-loaded imports remain in the import address table (IAT). However, if you use /delay:unload on the linker command line, the helper function will support the explicit unloading of the DLL, resetting the IAT to its original form; the now-invalid pointers will be overwritten. The IAT is a field in the [ImgDelayDescr](../vs140/Calling-Conventions--Parameters--and-Return-Type.md) that contains the address of a copy of the original IAT (if it exists).  
  
## Example  
  
### Code  
  
```  
// link with /link /DELAYLOAD:MyDLL.dll /DELAY:UNLOAD  
#include <windows.h>  
#include <delayimp.h>  
#include "MyDll.h"  
#include <stdio.h>  
  
#pragma comment(lib, "delayimp")  
#pragma comment(lib, "MyDll")  
int main()  
{  
    BOOL TestReturn;  
    // MyDLL.DLL will load at this point  
    fnMyDll();  
  
    //MyDLL.dll will unload at this point  
    TestReturn = __FUnloadDelayLoadedDLL2("MyDll.dll");  
  
    if (TestReturn)  
        printf_s("\nDLL was unloaded");  
    else  
        printf_s("\nDLL was not unloaded");  
}  
```  
  
### Comments  
 Important notes on unloading a delay-loaded DLL:  
  
-   You can find the implementation of the **__FUnloadDelayLoadedDLL2** function in the file \VC7\INCLUDE\DELAYHLP.CPP.  
  
-   The name parameter of the **__FUnloadDelayLoadedDLL2** function must exactly match (including case) what the import library contains (that string is also in the import table in the image). You can view the contents of the import library with [DUMPBIN /DEPENDENTS](../vs140/-DEPENDENTS.md). If a case-insensitive string match is desired, you can update **__FUnloadDelayLoadedDLL2** to use one of the CRT string functions or a Windows API call.  
  
 See [Unloading a Delay-Loaded DLL](../vs140/Unloading-a-Delay-Loaded-DLL.md) for more information.  
  
## See Also  
 [Linker Support for Delay-Loaded DLLs](../vs140/Linker-Support-for-Delay-Loaded-DLLs.md)