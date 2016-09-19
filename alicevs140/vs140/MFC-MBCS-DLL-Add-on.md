---
title: "MFC MBCS DLL Add-on"
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
ms.assetid: bebec0ff-e019-42ca-b5df-8c218ac5b54a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC MBCS DLL Add-on
In Visual Studio 2015, the MFC library for multibyte character encoding (MBCS) is included in the Visual C++ setup components. Visual C++ and MFC are optional install configurations in Visual Studio setup. To make sure that MFC is installed, choose **Custom** in setup, and under **Programming Languages**, make sure that **Visual C++** and **Microsoft Foundation Classes for C++** are selected. If you have already installed Visual Studio, you will be prompted to install Visual C++ and/or MFC when you attempt to create an MFC project.  
  
 You need the multibyte DLLs in order to build an MFC project in Visual Studio 2015 that has the **Character Set** property set to **Use Multi-Byte Character Set** or **Not Set**.  
  
## See Also  
 [MFC Library Versions](../vs140/MFC-Library-Versions.md)