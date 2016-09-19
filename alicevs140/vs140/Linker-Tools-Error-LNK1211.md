---
title: "Linker Tools Error LNK1211"
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
ms.topic: error-reference
ms.assetid: 607400eb-4180-4892-817f-eedfa628af61
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1211
precompiled type information not found; 'filename' not linked or overwritten  
  
 The given object file, compiled with [/Yc](../vs140/-Yc--Create-Precompiled-Header-File-.md), was not specified in the LINK command or was overwritten.  
  
 If you are creating a debug library that uses precompiled headers and if you specify /Yc and [/Z7](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md), Visual C++ generates a precompiled object file that contains CodeView debugging information. The error occurs only when you store the precompiled object file in a library, use the library to build an executable image, and the object files that are referenced have no transitive references to any of the functions the precompiled object file defines.  
  
 There are two methods to work around this situation:  
  
-   Specify the [/Yd](../vs140/-Yd--Place-Debug-Information-in-Object-File-.md) compiler option to add the CodeView information from the precompiled header to each object module. This method is less desirable because it generally produces large object modules that can increase the time required to link the application.  
  
-   Specify [/Yl](../vs140/-Yl--Inject-PCH-Reference-for-Debug-Library-.md) and pass the name of any arbitrary string, when you create a precompiled header file that does not contain any function definitions. This directs the compiler to create a symbol in the precompiled object file and to emit a reference to that symbol in each object file that used the precompiled header file that is associated with the precompiled object file.  
  
 When you compile a module with **/Yc** and **/Yl**, the compiler creates a symbol similar to `__@@_PchSym_@00@...@symbol_name`, where the ellipsis (...) represents a compiler-generated character string, and stores it in the object module. Any source file that you compile with this precompiled header refers to the specified symbol, which causes the linker to include the object module and its debugging information from the library.  
  
 For more information on this error, see Knowledge Base article Q102697 PRB: Build Errors Using Precompiled Header in Debugging Lib.