---
title: "Compiler Error C2144"
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
ms.assetid: 49f3959b-324f-4c06-9588-c0ecef5dc5b3
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2144
syntax error : 'type' should be preceded by 'token'  
  
 The compiler expected `token` and found `type` instead.  
  
 This error may be caused by a missing closing brace, right parenthesis, or semicolon.  
  
 C2144 can also occur when attempting to create a macro from a CLR keyword that contains a white space character.  
  
 You may also see C2144 if you are trying to do type forwarding. See [Type Forwarders](../vs140/Type-Forwarding--C---CLI-.md) for more information.  
  
## Example  
 The following sample generates C2144.  
  
```  
// C2144.cpp  
// compile with: /clr /c  
#define REF ref  
REF struct MyStruct0;   // C2144  
  
// OK  
#define REF1 ref struct  
REF1 MyStruct1;  
```  
  
## Example  
 The following sample generates C2144.  
  
```  
// C2144_2.cpp  
// compile with: /clr /c  
ref struct X {  
  
   property double MultiDimProp[,,] {   // C2144  
   // try the following line instead  
   // property double MultiDimProp[int , int, int] {  
      double get(int, int, int) { return 1; }  
      void set(int i, int j, int k, double l) {}  
   }  
  
   property double MultiDimProp2[] {   // C2144  
   // try the following line instead  
   // property double MultiDimProp2[int] {  
      double get(int) { return 1; }  
      void set(int i, double l) {}  
   }  
};  
```