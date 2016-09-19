---
title: "Project Build Error PRJ0024"
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
ms.assetid: 8bde6368-6c1b-4e04-bc5e-3c6d0b8fa1d7
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Build Error PRJ0024
Unicode path 'path' could not be translated to user's ANSI code page.  
  
 ***path***  is the original Unicode version of the path string. This error can occur in cases where there is a Unicode path that cannot be directly translated to ANSI for the current system code page.  
  
 This error may occur if you are working with a project that was developed on a system using a code page that is not on your computer.  
  
 The resolution for this error is to update the path to use ANSI text or to install the code page on your computer and set it as the system default.