---
title: "Project Build Warning PRJ0041"
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
ms.assetid: dc9f4cf9-6bd5-4222-89e8-7802a59bb96b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Build Warning PRJ0041
Cannot find missing dependency 'dependency' for file 'file'. Your project may still build, but may continue to appear out of date until this file is found.  
  
 A file (resource file or .idl/.odl file, for example, contained an include statement that the project system could not resolve.  
  
 Because the project system does not process preprocessor statements (#if, for example), the offending statement may not actually be part of the build.  
  
 To resolve this warning, delete all unnecessary code in .rc files or add placeholder files of the appropriate name.