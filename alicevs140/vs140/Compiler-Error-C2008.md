---
title: "Compiler Error C2008"
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
ms.assetid: e748ccbe-ffd4-4008-aca7-e53c25225209
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2008
'character' : unexpected in macro definition  
  
 The character appears immediately following the macro name. To resolve the error, there must be a space after the macro name.  
  
 The following sample generates C2008:  
  
```  
// C2008.cpp  
#define TEST1"mytest1"    // C2008  
```  
  
 Possible resolution:  
  
```  
// C2008b.cpp  
// compile with: /c  
#define TEST2 "mytest2"  
```