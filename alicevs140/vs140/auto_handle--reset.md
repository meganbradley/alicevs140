---
title: "auto_handle::reset"
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
ms.topic: reference
ms.assetid: 32dc3a83-80fd-45c9-8f79-8c4096c30f57
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_handle::reset
Destroy the current owned object and optionally take possession of a new object.  
  
## Syntax  
  
```  
void reset(  
   _element_type ^ _new_ptr  
);  
void reset();  
```  
  
#### Parameters  
 `_new_ptr`  
 (Optional) The new object.  
  
## Example  
  
```  
// msl_auto_handle_reset.cpp  
// compile with: /clr  
#include <msclr\auto_handle.h>  
  
using namespace System;  
using namespace msclr;  
  
ref class ClassA {  
   String^ m_s;  
public:  
   ClassA( String^ s ) : m_s( s ) {  
      Console::WriteLine( "ClassA constructor: " + m_s );  
   }  
   ~ClassA() {  
      Console::WriteLine( "ClassA destructor: " + m_s );  
   }  
  
   void PrintHello() {  
      Console::WriteLine( "Hello from {0} A!", m_s );  
   }  
};  
  
int main()  
{  
   auto_handle<ClassA> agc1 = gcnew ClassA( "first" );  
   agc1->PrintHello();  
  
   ClassA^ ha = gcnew ClassA( "second" );  
   agc1.reset( ha ); // release first object, reference second  
   agc1->PrintHello();  
  
   agc1.reset(); // release second object, set to nullptr  
  
   Console::WriteLine( "done" );  
}  
```  
  
 **ClassA constructor: first**  
**Hello from first A!**  
**ClassA constructor: second**  
**ClassA destructor: first**  
**Hello from second A!**  
**ClassA destructor: second**  
**done**   
## Requirements  
 **Header file** <msclr\auto_handle.h>  
  
 **Namespace** msclr  
  
## See Also  
 [auto_handle Members](../vs140/auto_handle-Members.md)   
 [auto_handle::release](../vs140/auto_handle--release.md)