---
title: "Project Build Error PRJ0008"
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
ms.assetid: 6bf7f17a-d2a8-4826-99c7-d600d846952f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Build Error PRJ0008
Could not delete file 'file'.  
  
 **Make sure that the file is not open by another process and is not write-protected.**  
  
 During a rebuild or clean, Visual C++ deletes all known intermediate and output files for the build, as well as any files that meet the wildcard specifications in the **Extensions to Delete on Clean** property in the [General Configuration Settings Property Page](../Topic/General%20Property%20Page%20\(Project\).md).  
  
 You will see this error if Visual C++ is not able to delete a file. To resolve the error, make the file and its directory writeable for the user doing the build.