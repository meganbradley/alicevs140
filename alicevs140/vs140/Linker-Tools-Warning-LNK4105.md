---
title: "Linker Tools Warning LNK4105"
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
ms.assetid: 6c7bebf4-4ea6-4533-a6ed-e563d43abbd7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4105
no argument specified with option 'option'; ignoring option  
  
 This warning occurs only when the [/LIBPATH](../vs140/-LIBPATH--Additional-Libpath-.md) option is set. If no directory is specified with this option, then the linker ignores the option and generates this warning message.  
  
 If you do not need to override the existing environmental library settings, remove the /LIBPATH option from the linker command line. If you want to use an alternate search path for libraries, specify the alternate path following the /LIBPATH option.  
  
## Example  
  
```  
link /libpath:c:\filepath\lib bar.obj  
```  
  
 would direct the linker to search for the required libraries in `c:\filepath\lib` before searching in the default locations.