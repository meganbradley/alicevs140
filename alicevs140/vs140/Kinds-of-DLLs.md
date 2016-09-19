---
title: "Kinds of DLLs"
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
ms.assetid: f6a30db9-6138-4b2c-90cc-a17855e499a6
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Kinds of DLLs
This topic provides information to help you determine the kind of DLL to build.  
  
##  <a name="_core_the_different_kinds_of_dlls_available_with_visual_c.2b2b"></a> Different Kinds of DLLs Available  
 Using Visual C++, you can build Win32 DLLs in C or C++ that do not use the Microsoft Foundation Class (MFC) library. You can create a non-MFC DLL project with the Win32 Application Wizard.  
  
 The MFC library itself is available, in either static link libraries or in a number of DLLs, with the MFC DLL Wizard. If your DLL is using MFC, Visual C++ supports three different DLL development scenarios:  
  
-   Building a regular DLL that statically links MFC  
  
-   Building a regular DLL that dynamically links MFC  
  
-   Building an MFC extension DLL, which always dynamically link MFC  
  
### What do you want to know more about?  
  
-   [Non-MFC DLLs: Overview](../vs140/Non-MFC-DLLs--Overview.md)  
  
-   [Regular DLLs statically linked to MFC](../vs140/Regular-DLLs-Statically-Linked-to-MFC.md)  
  
-   [Regular DLLs dynamically linked to MFC](../vs140/Regular-DLLs-Dynamically-Linked-to-MFC.md)  
  
-   [Extension DLLs: Overview](../vs140/Extension-DLLs--Overview.md)  
  
-   [Which kind of DLL to use](#_core_which_kind_of_dll_to_use)  
  
##  <a name="_core_which_kind_of_dll_to_use"></a> Deciding Which Kind of DLL to Use  
 If your DLL does not use MFC, use Visual C++ to build a non-MFC Win32 DLL. Linking your DLL to MFC (either statically or dynamically) takes up significant disk space and memory. You should not link to MFC unless your DLL actually uses MFC.  
  
 If your DLL will be using MFC, and will be used by either MFC or non-MFC applications, you must build either a regular DLL that dynamically links to MFC or a regular DLL that statically links to MFC. In most cases, you probably want to use a regular DLL that dynamically links to MFC because the file size of the DLL will be much smaller and the savings in memory from using the shared version of MFC can be significant. If you statically link to MFC, the file size of your DLL will be larger and potentially take up extra memory because it loads its own private copy of the MFC library code.  
  
 Building a DLL that dynamically links to MFC is faster than building a DLL that statically links to MFC because it is not necessary to link MFC itself. This is especially true in debug builds where the linker must compact the debug information. By linking with a DLL that already contains the debug information, there is less debug information to compact within your DLL.  
  
 One disadvantage to dynamically linking to MFC is that you must distribute the shared DLLs Mfcx0.dll and Msvcrxx.dll (or similar files) with your DLL. The MFC DLLs are freely redistributable, but you still must install the DLLs in your setup program. In addition, you must ship the Msvcrxx.dll, which contains the C run-time library that is used both by your program and the MFC DLLs themselves.  
  
 If your DLL will only be used by MFC executables, you have a choice between building a regular DLL or an extension DLL. If your DLL implements reusable classes derived from the existing MFC classes or you need to pass MFC-derived objects between the application and the DLL, you must build an extension DLL.  
  
 If your DLL dynamically links to MFC, the MFC DLLs might be redistributed with your DLL. This architecture is particularly useful for sharing the class library between multiple executable files to save disk space and minimize memory usage.  
  
 Prior to version 4.0, Visual C++ only supported two kinds of DLLs that used MFC: USRDLLs and AFXDLLs. Regular DLLs statically linked to MFC have the same characteristics as the former USRDLL. MFC extension DLLs have the same characteristics as the former AFXDLLs.  
  
### What do you want to know more about?  
  
-   [Non-MFC DLLs: Overview](../vs140/Non-MFC-DLLs--Overview.md)  
  
-   [Regular DLLs statically linked to MFC](../vs140/Regular-DLLs-Statically-Linked-to-MFC.md)  
  
-   [Regular DLLs dynamically linked to MFC](../vs140/Regular-DLLs-Dynamically-Linked-to-MFC.md)  
  
-   [Extension DLLs: Overview](../vs140/Extension-DLLs--Overview.md)  
  
## See Also  
 [DLLs in Visual C++](../vs140/DLLs-in-Visual-C--.md)