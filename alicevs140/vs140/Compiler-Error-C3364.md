---
title: "Compiler Error C3364"
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
ms.assetid: 98654741-60fe-4472-a6af-e580f8c0a6e1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3364
'delegate': delegate constructor: argument must be pointer to member function of managed class or global function  
  
 The second parameter of the delegate's constructor takes either the address of a member function or the address of a static member function of any class. Both are treated as simple addresses.  
  
 The following sample generates C3364:  
  
```  
// C3364_2.cpp  
// compile with: /clr  
  
delegate int D( int, int );  
  
ref class C {  
public:  
   int mf( int, int ) {  
      return 1;  
   }  
};  
  
int main() {  
   C^ pC = gcnew C;  
   System::Delegate^ pD = gcnew D( pC,pC->mf( 1, 2 ) ); // C3364  
  
   // try the following line instead  
   // System::Delegate^ pD = gcnew D(pC, &C::mf);  
}  
```  
  
 The following sample generates C3364:  
  
```  
// C3364.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
  
__delegate int D(int, int);  
  
__gc class C {  
public:  
   int mf(int, int) {  
      return 1;  
   }  
};  
  
int main() {  
   C *pC = new C;  
   System::Delegate *pD = new D(pC, pC->mf(1, 2));   // C3364  
   // try the following line instead  
   // System::Delegate *pD = new D(pC, &C::mf);  
}  
```