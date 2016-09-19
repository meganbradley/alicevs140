---
title: "Compiler Error C2388"
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
ms.assetid: 764ad2d7-cb04-425f-ba30-70989488c4a4
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2388
'symbol' : a symbol cannot be declared with both __declspec(appdomain) and \__declspec(process)  
  
 The `appdomain` and `process``__declspec` modifiers cannot be used on the same symbol. The storage for a variable exists per process or per application domain.  
  
 For more information, see [appdomain](../vs140/appdomain.md) and [process](../vs140/process.md).  
  
 The following sample generates C2388:  
  
```  
// C2388.cpp  
// compile with: /clr /c  
__declspec(process) __declspec(appdomain) int i;   // C2388  
__declspec(appdomain) int i;   // OK  
```