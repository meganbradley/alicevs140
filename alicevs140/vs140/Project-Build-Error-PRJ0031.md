---
title: "Project Build Error PRJ0031"
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
ms.assetid: b42435c6-e570-4f8e-9ad5-12a7ea69ccb2
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Build Error PRJ0031
The 'Outputs' property for the custom build step for file 'file' contained 'macro' which evaluates out to 'macro_expansion'.  
  
 A custom build step on a file had bad output probably due to a macro evaluation problem. This error could also mean that the path is badly formed, containing characters or combinations of characters that are illegal in a file path.  
  
 To resolve this error, fix the macro or fix the path specification. The evaluated path is an absolute path from the project directory.