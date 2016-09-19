---
title: "Compiler Error C2198"
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
ms.assetid: 638a845c-9d7f-4115-a9aa-d72455605668
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2198
'function' : too few arguments for call  
  
 The compiler found too few parameters for a call to the function, or an incorrect function declaration.  
  
 The following sample generates C2198:  
  
```  
// C2198.c  
// compile with: /c  
void func( int, int );  
int main() {  
   func( 1 );   // C2198 only one actual parameter  
   func( 1, 1 );   // OK  
}  
```