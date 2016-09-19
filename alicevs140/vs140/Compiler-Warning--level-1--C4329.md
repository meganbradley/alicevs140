---
title: "Compiler Warning (level 1) C4329"
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
ms.assetid: 4316f51a-2c56-4b3f-831e-65d24b83b65c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4329
__declspec(align()) is ignored on enum  
  
 Use of the [align](../vs140/align--C---.md) keyword of the [__declspec](../vs140/__declspec.md) modifier is not allowed on an `enum`. The following sample generates C4329:  
  
```  
// C4329.cpp  
// compile with: /W1 /LD  
enum __declspec(align(256)) TestEnum {   // C4329  
   TESTVAL1,  
   TESTVAL2,  
   TESTVAL3  
};  
__declspec(align(256)) enum TestEnum1;  
```