---
title: "Fatal Error C1018"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2ceb8a99-30b2-4b80-bf42-e9f3305b3c52
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1018
unexpected #elif  
  
 The `#elif` directive appears outside an `#if`, `#ifdef`, or `#ifndef` construct. Use `#elif` only within one of these constructs.  
  
 The following sample generates C1018:  
  
```  
// C1018.cpp  
#elif      // C1018  
#endif  
  
int main() {}  
```  
  
 Possible resolution:  
  
```  
// C1018b.cpp  
#if 1  
#elif  
#endif  
  
int main() {}  
```