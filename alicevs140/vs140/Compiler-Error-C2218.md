---
title: "Compiler Error C2218"
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
ms.assetid: b0f55da4-8edb-4b45-b298-1a091981bd7b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2218
'__vectorcall' cannot be used with '/arch:IA32'  
  
 The `__vectorcall` calling convention is only supported in native code on x86 and x64 processors that include Streaming SIMD Extensions 2 (SSE2) and above. For more information, see [__vectorcall](../vs140/__vectorcall.md).  
  
 To fix this error, change the compiler options to target SSE2, AVX or AVX2 instruction sets. For more information, see [/arch (x86)](../vs140/-arch--x86-.md).