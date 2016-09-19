---
title: "NMAKE Fatal Error U1064"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 7141e66e-cde6-4173-84df-a391f3ebcdd1
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NMAKE Fatal Error U1064
MAKEFILE not found and no target specified  
  
 The NMAKE command line did not specify a makefile or a target, and the current directory did not contain a file named MAKEFILE.  
  
 NMAKE requires either a makefile or a command-line target (or both). To make a makefile available to NMAKE, either specify the /F option or place a file named MAKEFILE in the current directory. NMAKE can create a command-line target by using an inference rule if a makefile is not provided.