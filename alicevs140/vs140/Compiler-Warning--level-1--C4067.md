---
title: "Compiler Warning (level 1) C4067"
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
ms.assetid: 1d10353e-8cd5-4b01-9184-a06189b965a4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4067
unexpected tokens following preprocessor directive - expected a newline  
  
 The compiler found and ignored extra characters following a preprocessor directive. This warning appears only under ANSI compatibility ([/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)).  
  
```  
// C4067a.cpp  
// compile with: /DX /Za /W1  
#pragma warning(default:4067)  
#if defined(X)  
#else  
#endif v   // C4067  
int main()  
{  
}  
```  
  
### To resolve this warning, try the following:  
  
1.  Compile with **/Ze**.  
  
2.  Use comment delimiters:  
  
```  
// C4067b.cpp  
// compile with: /DX /Za /W1  
#if defined(X)  
#else  
#endif  
int main()  
{  
}  
```