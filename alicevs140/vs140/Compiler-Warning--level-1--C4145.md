---
title: "Compiler Warning (level 1) C4145"
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
ms.assetid: 0440777a-cca2-4159-aff5-e67a254ad64a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4145
'expression1' : relational expression as switch expression; possible confusion with 'expression2'  
  
 A `switch` statement uses a relational expression as its control expression, which results in a Boolean value for the **case** statements. Did you mean *expression2*?  
  
## Example  
 The following sample generates C4145:  
  
```  
// C4145.cpp  
// compile with: /W1  
int main() {  
   int i = 0;  
   switch(i == 1) {   // C4145, use i instead of i == 1 to resolve  
      case 1:  
         break;  
      default:  
         break;  
   }  
}  
```