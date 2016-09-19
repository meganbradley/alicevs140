---
title: "Project Build Error PRJ0044"
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
ms.assetid: 5d78c45a-f9e9-4d2b-a3b6-5a5d1421ab84
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Build Error PRJ0044
The 'Additional Dependencies' property for custom build rule 'rule' assigned to file 'file' is invalid. The property contained 'string' which evaluates to 'value'.  
  
 The **Additional Dependencies** property evaluated to an empty string, or to a string that contained invalid characters (any character that could not be in a file or directory name). Custom build rules need the output of the build action.  
  
 For more information, see [Specifying Custom Build Tools](../vs140/Specifying-Custom-Build-Tools.md).  
  
## See Also  
 [Project Build Errors and Warnings (PRJxxxx)](../vs140/Project-Build-Errors-and-Warnings--PRJxxxx-.md)