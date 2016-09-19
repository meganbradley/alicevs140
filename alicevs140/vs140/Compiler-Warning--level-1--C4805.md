---
title: "Compiler Warning (level 1) C4805"
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
ms.topic: error-reference
ms.assetid: 99c7b7e2-272e-4ab5-8580-17c42e62e2ef
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4805
'operation' : unsafe mix of type 'type' and type 'type' in operation  
  
 This warning is generated for comparison operations between [bool](../vs140/bool--C---.md) and [int](../vs140/Integer-Types.md). The following sample generates C4805:  
  
```  
// C4805.cpp  
// compile with: /W1  
int main() {  
   int i = 1;  
   bool b = true;  
  
   if (i == b) {   // C4805, comparing bool and int variables  
   }  
}  
```