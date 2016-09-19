---
title: "Project Build Error PRJ0025"
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
ms.assetid: 57725c78-bc63-44f3-9667-2969b2d7c41d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Build Error PRJ0025
Batch file 'file' contains Unicode contents that could not be translated to user's ANSI code page.  
  
 ***UNICODE contents of file***  
  
 The project system found Unicode contents in a custom build rule or build event that cannot be translated properly to the user's current ANSI code page.  
  
 The resolution for this error is to update the contents of the build rule or build event to use ANSI or to install the code page on your computer and set it as the system default.  
  
 For more information on custom build steps and build events, see [Understanding Custom Build Steps and Build Events](../vs140/Understanding-Custom-Build-Steps-and-Build-Events.md).