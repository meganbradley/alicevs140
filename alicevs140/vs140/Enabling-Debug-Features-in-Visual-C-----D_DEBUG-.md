---
title: "Enabling Debug Features in Visual C++ (-D_DEBUG)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
H1: Enabling Debug Features in Visual C++ (/D_DEBUG)
ms.assetid: 276e2254-7274-435e-ba4d-67fcef4f33bc
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Enabling Debug Features in Visual C++ (-D_DEBUG)
In [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)], debugging features such as assertions are enabled when you compile your program with the symbol **_DEBUG** defined. You can define **_DEBUG** in one of two ways:  
  
-   Specify **#define _DEBUG** in your source code, or  
  
-   Specify the **/D_DEBUG** compiler option. (If you create your project in Visual Studio using wizards, **/D_DEBUG** is defined automatically in the Debug configuration.)  
  
 When **_DEBUG** is defined, the compiler compiles sections of code surrounded by **#ifdef _DEBUG** and `#endif`.  
  
 The Debug configuration of an MFC program must link with a Debug version of the MFC library. The MFC header files determine the correct version of the MFC library to link with based on the symbols you have defined, such as **_DEBUG** and **_UNICODE**. For details, see [MFC Library Versions](../vs140/MFC-Library-Versions.md).  
  
## See Also  
 [Debugging Native Code](../vs140/Debugging-Native-Code.md)   
 [Project Settings for a C++ Debug Configuration](../Topic/Project%20Settings%20for%20a%20C++%20Debug%20Configuration.md)