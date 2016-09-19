---
title: "Using Precompiled Headers in a Project"
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
ms.assetid: 95010260-a035-4327-9d61-222016ac146c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Precompiled Headers in a Project
Previous sections present an overview of precompiled headers: /Yc and /Yu, the /Fp option, and the [hdrstop](../vs140/hdrstop.md) pragma. This section describes a method for using the manual precompiled-header options in a project; it ends with an example makefile and the code that it manages.  
  
 For another approach to using the manual precompiled-header options in a project, study one of the makefiles located in the MFC\SRC directory that is created during the default setup of Visual C++. These makefiles take a similar approach to the one presented in this section but make greater use of Microsoft Program Maintenance Utility (NMAKE) macros, and offer greater control of the build process.  
  
 This section contains the following topics:  
  
-   [PCH Files in the Build Process](../vs140/PCH-Files-in-the-Build-Process.md)  
  
-   [Sample Makefile for PCH](../vs140/Sample-Makefile-for-PCH.md)  
  
-   [Example Code for PCH](../vs140/Example-Code-for-PCH.md)  
  
## See Also  
 [Creating Precompiled Header Files](../vs140/Creating-Precompiled-Header-Files.md)