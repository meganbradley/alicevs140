---
title: "Compiler Warning C4801"
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
ms.assetid: 05b29dff-15ef-42ca-9712-dc993afc4fd6
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning C4801
Return by reference is not verifiable: reason  
  
 You cannot store a tracking reference into a local variable and then return it verifiably.  
  
 A reference can only be verifiably returned when it can be tracked by the verifier from creation to return point and when it is a reference to an element of an array, or a member of a class.  
  
 For more information, see [PEVerify Tool (Peverify.exe)](assetId:///f4f46f9e-8d08-4e66-a94b-0c69c9b0bbfa).  
  
 A reference must remain on the stack from creation to return in order to be verifiable.  
  
 C4801 is always issued as an error.  You can turn off this warning with the `#pragma warning` or **/wd**; see [warning](../vs140/warning.md) or [/w, /Wn, /WX, /Wall, /wln, /wdn, /wen, /won (Warning Level)](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md) for more information.  
  
## Example  
 C4801 will be generated if the verifier cannot see the address taken, so it must assume that it might be an unverifiable reference. The following sample generates C4801.  
  
```  
// C4801.cpp  
// compile with: /clr:safe /c  
int% f(int% p) {  
   return p;   // C4801  
}  
```  
  
## Example  
 The following sample generates C4801.  
  
```  
// C4801_b.cpp  
// compile with: /clr:safe /c  
  
int% f(int i, array<int>^ ar) {  
   int x;  
   int% bri = x;   // cannot return a byref to a local.  
   if (i < ar->Length) {  
      bri = ar[i];   // this byref is ok.  
   }  
  
   return bri;   // C4801 not returned within the basic block  
}  
```  
  
## Example  
 C4801 can also occur if you attempt to dereference and return a reference value in a try block. This will result in code that cannot be verified because the stack is cleared at the end of a try block, destroying any return value on the stack. Instead, dereference the reference type and assign it to a variable, to ensure that no exception is thrown. Then, at the end of the function, dereference the reference type again and return it.  
  
 The following sample generates C4801.  
  
```  
// C4801_c.cpp  
// compile with: /clr:safe  
using namespace System;  
  
ref class StackEmptyException : public System::Exception {};  
ref class StackFullException : public System::Exception {};  
  
template <typename T>  
ref struct Stack {  
  
   Stack() {  
      topElem = -1;   // initialize stack  
      stackPtr = gcnew array<T>(10);  
   }  
  
   void push(const T%);  
   T% top();  
  
private:  
   int topElem;    
   array<T>^ stackPtr;    
};  
  
template <typename T>   
T% Stack<T>::top() {  
   try {  
      return stackPtr[topElem];   // C4801  
      // Try the following line instead.  
      // T% deadstore = stackPtr[topElem] ;  
   }  
  
   catch (System::IndexOutOfRangeException ^ e) {  
      throw gcnew StackEmptyException();  
   }  
  
   catch (System::Exception ^ e) {  
      throw;  
   }  
  
   return stackPtr[topElem] ;  
}  
  
int main() {  
   typedef Stack<Int32> IntStack;  
   IntStack ^ is = gcnew IntStack();  
  
   int i = 1;  
   while (1) {  
      try {  
         is->push(i++);  
      }  
      catch (System::Exception ^ e) {  
         break;  
      }  
      Console::Write("{0} ", is->top());  
   }  
}  
```