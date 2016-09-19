---
title: "Resource Compiler Error RC2180"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6d296138-7989-491e-a45b-6c3a4743116a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Resource Compiler Error RC2180
unable to open temporary file  
  
 The Resource Compiler/Visual C++ was unable to open a temporary file. The probable cause is either that you do not have write permissions for the directory, or that the directory does not exist. The Resource Compiler/Visual C++ attempts to use these files in the directory specified by the **TMP** environment variable or the current directory if none is specified.