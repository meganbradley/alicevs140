---
title: "Compiler Error C3162"
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
ms.assetid: 0d4c4a24-1456-4191-b7d8-c38cb7b17c32
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3162
'type' : a reference type which has a destructor cannot be used as the type of static data member 'member'  
  
 The common language runtime cannot know when to run a user-defined destructor when the class also contains static member function.  
  
 A destructor will never be run unless the object is deleted explicitly.  
  
 For more information, see,  
  
-   [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md)  
  
-   [Common 64-bit Migration Issues](../vs140/Common-Visual-C---64-bit-Migration-Issues.md)  
  
## Example  
 The following sample generates C3162.  
  
```  
// C3162.cpp  
// compile with: /clr /c  
ref struct A {  
   ~A() { System::Console::WriteLine("in destructor"); }  
   static A i;   // C3162  
   static A^ a = gcnew A;   // OK  
};  
  
int main() {  
   A ^ a = gcnew A;  
   delete a;  
}  
```