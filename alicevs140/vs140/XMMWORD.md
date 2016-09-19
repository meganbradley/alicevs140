---
title: "XMMWORD"
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
ms.topic: article
ms.assetid: 18026d32-5cab-403e-ad7e-382fb41aa9b8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XMMWORD
Used for 128-bit multimedia operands with MMX and SSE (XMM) instructions.  
  
## Syntax  
  
```  
XMMWORD  
```  
  
## Remarks  
 `XMMWORD` is intended to represent the same type as [__m128](../vs140/__m128.md).  
  
## Example  
  
```  
movdqa   xmm0, xmmword ptr [ebx]  
```