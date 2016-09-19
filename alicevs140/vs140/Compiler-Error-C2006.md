---
title: "Compiler Error C2006"
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
ms.assetid: caaed6f7-ceb9-4742-8820-d66657c0b04d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2006
'directive' expected a filename, found 'token'  
  
 Directives such as [#include](../vs140/#include-Directive--C-C---.md) or [#import](../vs140/#import-Directive--C---.md) require a filename. To resolve the error, make sure *token* is a valid filename. Also, put the filename in double quotes or angle brackets.  
  
 The following sample generates C2006:  
  
```  
// C2006.cpp  
#include stdio.h   // C2006  
```  
  
 Possible resolution:  
  
```  
// C2006b.cpp  
// compile with: /c  
#include <stdio.h>  
```