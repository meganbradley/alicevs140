---
title: "Fatal Error C1016"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 33f45c3e-2d8f-43ad-a445-c412d1d54ce1
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1016
\#ifdef expected an identifier#ifndef expected an identifier  
  
 The conditional compilation directive ([#ifdef](../vs140/#ifdef-and-#ifndef-Directives--C-C---.md) or `#ifndef`) has no identifier to evaluate. To resolve the error, specify an identifier.  
  
 The following sample generates C1016:  
  
```  
// C1016.cpp  
#ifdef   // C1016  
#define FC1016  
#endif  
  
int main() {}  
```  
  
 Possible resolution:  
  
```  
// C1016b.cpp  
#ifdef X  
#define FC1016  
#endif  
  
int main() {}  
```