---
title: "Compiler Error C3416"
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
ms.assetid: 53a79fb9-42da-4f61-8939-133b370f7edf
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3416
'function' : an explicit specialization may not be explicitly instantiated  
  
 A function cannot be both explicitly specialized and explicitly instantiated.  
  
 The following sample generates C3416:  
  
```  
// C3416.cpp  
template <class T>   
void f();  
  
template <>   
void f<int>() {}  
template void f<int>();   // C3416 delete this or previous line to resolve  
```