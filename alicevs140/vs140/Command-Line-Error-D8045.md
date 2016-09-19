---
title: "Command-Line Error D8045"
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
ms.assetid: 01c8808c-bac1-4b4d-8a90-b595f95e9318
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Command-Line Error D8045
cannot compile C file 'file' with the /clr option  
  
 Only C++ source code files can be passed to a compilation that uses **/clr**.  Use **/TP** to compile a .c file as a .cpp file; see [/Tc, /Tp, /TC, /TP (Specify Source File Type)](../vs140/-Tc---Tp---TC---TP--Specify-Source-File-Type-.md) for more information.  
  
 For more information, see [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
 D8045 can also occur if you compile an ATL application using Visual C++. See [How To: Migrate to /clr](../vs140/How-to--Migrate-to--clr.md) for more information.