---
title: "Compiler Warning (level 1) C4684"
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
ms.assetid: e95f1a83-2784-4b05-ae94-12148e056e26
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4684
'attribute' : WARNING!! attribute may cause invalid code generation: use with caution  
  
 You used an attribute that should not commonly be used.  
  
 The following sample generates C4684:  
  
```  
// C4684.cpp  
// compile with: /W1 /LD  
 [module(name="xx")]; // C4684 expected  
[no_injected_text];  
```