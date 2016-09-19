---
title: "Fatal Error C1037"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 79103bca-ccfb-42e7-aef9-9b90c15b162f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1037
cannot open object file filename  
  
 The object file specified by [/Fo](../Topic/-Fo%20\(Object%20File%20Name\).md) cannot be opened.  
  
### To fix by checking the following possible causes  
  
1.  Invalid filename.  
  
2.  Insufficient memory to open the file.  
  
3.  Another process is using the file.  
  
4.  A read-only file has the same name.  
  
 In Visual C++ .NET (version 1300 of the compiler), there is a bug that requires the user locale to be set correctly when the file name (or directory path to the file name) contains MBCS characters. Setting the system locale is not sufficient; the user locale must be set to process MBCS characters.