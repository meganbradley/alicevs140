---
title: "Fatal Error C1047"
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
ms.assetid: e1bbbc6b-a5bc-4c23-8203-488120a0ec78
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1047
The object or library file 'file' was created with an older compiler than other objects; rebuild old objects and libraries  
  
 C1047 is caused when object files or libraries built with **/LTCG** are linked together, but where those object files or libraries are built with different versions of the Visual C++ toolset.  
  
 This can happen if you begin using a new version of the compiler but do not do a clean rebuild of existing object files or libraries.  
  
 To resolve C1047, rebuild all object files or libraries.