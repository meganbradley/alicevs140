---
title: "Compiler Warning (level 1) C4342"
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
ms.assetid: 47d4d5ab-069f-4cdc-98c3-10d649577a37
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4342
behavior change: 'function' called, but a member operator was called in previous versions  
  
 In previous versions of Visual C++, a member was called, but this behavior has been changed and the compiler will find the best match in namespace scope.  
  
 If a member operator was found, the compiler would previously not consider any namespace scope operators. If there is a better match at namespace scope, the current compiler will correctly call it, whereas previous compilers wouldn't consider it.  
  
 This warning should be disabled after you successfully port your code to the current version.  The compiler may give false positives, generating this warning for code where there is no behavior change.  
  
 This warning is off by default. For more information, see [Compiler Warnings That Are Off by Default](../vs140/Compiler-Warnings-That-Are-Off-by-Default.md).  
  
 The following sample generates C4342:  
  
```  
// C4342.cpp  
// compile with: /EHsc /W1  
#include <fstream>  
#pragma warning(default: 4342)  
using namespace std;  
struct X : public ofstream {  
   X();  
};  
  
X::X() {  
   open( "ofs_bug_ev.txt." );  
   if ( is_open() ) {  
      *this << "Text" << "<-should be text" << endl;   // C4342  
      *this << ' ' << "<-should be space symbol" << endl;   // C4342  
   }  
}  
  
int main() {  
   X b;  
   b << "Text" << "<-should be text" << endl;  
   b << ' ' << "<-should be space symbol" << endl;  
}  
```