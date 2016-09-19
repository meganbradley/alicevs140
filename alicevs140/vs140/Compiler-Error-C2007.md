---
title: "Compiler Error C2007"
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
ms.assetid: ecd09d99-5036-408b-9e46-bc15488f049e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2007
\#define syntax  
  
 No identifier appears after a `#define`. To resolve the error, use an identifier.  
  
 The following sample generates C2007:  
  
```  
// C2007.cpp  
#define   // C2007  
```  
  
 Possible resolution:  
  
```  
// C2007b.cpp  
// compile with: /c  
#define true 1  
```