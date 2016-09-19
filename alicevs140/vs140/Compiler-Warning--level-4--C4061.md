---
title: "Compiler Warning (level 4) C4061"
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
ms.assetid: a99cf88e-7941-4519-8b1b-f6889d914b2f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4061
enumerator 'identifier' in switch of enum 'enumeration' is not explicitly handled by a case label  
  
 The enumerate has no associated handler in a `switch` statement.  
  
 This warning is off by default. See [Compiler Warnings That Are Off by Default](../vs140/Compiler-Warnings-That-Are-Off-by-Default.md) for more information.  
  
 The following sample generates C4061:  
  
```  
// C4061.cpp  
// compile with: /W4  
#pragma warning(default : 4061)  
  
enum E { a, b, c };  
void func ( E e )  
{  
   switch(e)  
   {  
      case a:  
      case b:  
      default:  
         break;  
   }   // C4061 c' not handled  
}  
  
int main()  
{  
}  
```