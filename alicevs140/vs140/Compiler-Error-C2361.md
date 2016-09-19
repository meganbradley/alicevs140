---
title: "Compiler Error C2361"
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
ms.assetid: efbdaeb9-891c-4f7d-97da-89088a8413f3
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2361
initialization of 'identifier' is skipped by 'default' label  
  
 The initialization of `identifier` can be skipped in a `switch` statement. You cannot jump past a declaration with an initializer unless the declaration is enclosed in a block. (Unless it is declared within a block, the variable is within scope until the end of the `switch` statement.)  
  
 The following sample generates C2361:  
  
```  
// C2361.cpp  
void func( void ) {  
   int x;  
   switch (x) {  
   case 0 :  
      int i = 1;  
      { int j = 1; }  
   default :   // C2361 error  
      int k = 1;  
   }  
}  
```  
  
 Possible resolution:  
  
```  
// C2361b.cpp  
// compile with: /c  
void func( void ) {  
   int x = 0;  
   switch (x) {  
   case 0 :  
      { int j = 1; int i = 1;}  
   default :  
      int k = 1;  
   }  
}  
```