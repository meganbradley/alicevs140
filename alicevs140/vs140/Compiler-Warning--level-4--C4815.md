---
title: "Compiler Warning (level 4) C4815"
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
ms.assetid: 99081928-d7d5-4dce-b4af-7c6a151bfac0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4815
'var' : zero-sized array in stack object will have no elements (unless the object is an aggregate that has been aggregate initialized)  
  
 An array with an undefined number of elements (zero-sized array) is the last member of a type and an object of the type was created on the stack. No memory will be allocated for the array. If you need a useful constructor, you can allocate memory for the struct on the heap.  
  
 The following sample generates C4815:  
  
```  
// C4815.cpp  
// compile with: /W4  
#include <memory>  
#pragma warning(disable : 4200)  
struct S1  
{  
   int i;  
   char cArr[];  
};  
  
S1 s1_glb;   // C4815 stack object with zero-array (not aggregate inited)  
// try the following line instead  
// S1 s1_glb = { 0, 0, 0 };  
  
struct S2  
{  
   S2(int _i) : i(_i) {}  
   int i;  
   char cArr[];  
};  
  
S2 s2_glb1(10);   // C4815  
// try the following line instead  
// S2 s2_glb1 = { 10 };  // to work, comment the constructor  
  
int main()  
{  
   S1 s1_loc1;   // C4815  
   // try the following line instead  
   // S1 s1_loc1 = { 0 };  
  
   S1 s1_loc2 = { 1, { 'a', 'b', 'c' } };  
  
   S1 s1_loc3 = s1_loc2;   // C4815 truncation when copy ctor called  
   // truncation if call a compiler-generated copy constructor  
   // to copy a struct with a zero sized array in it  
   s1_loc1;  
   s1_loc2;  
   s1_loc3;  
  
   // allocate memory for struct on heap  
   int nEle = 10;   // allocate 10 chars for char array  
   void * pV = malloc (sizeof(S2) + nEle * sizeof(char));  
   S2 *pS1 = new (pV) S2(nEle);  
   pS1;  
}  
```