---
title: "Compiler Warning (level 1) C4939"
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
ms.assetid: 07096008-ba47-436c-a84c-2b03ad90d0b3
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4939
\#pragma vtordisp is deprecated and will be removed in a future release of Visual C++  
  
 The [vtordisp](../vs140/vtordisp.md) pragma will be removed in a future release of Visual C++.  
  
## Example  
 The following sample generates C4939.  
  
```  
// C4939.cpp  
// compile with: /c /W1  
#pragma vtordisp(off)   // C4939  
```