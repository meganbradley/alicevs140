---
title: "bad_typeid Exception"
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
ms.topic: language-reference
ms.assetid: 5963ed58-4ede-4597-957d-f7bbd06299c2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bad_typeid Exception
The `bad_typeid` exception is thrown by the [typeid operator](../Topic/typeid%20Operator.md) when the operand for `typeid` is a NULL pointer.  
  
## Syntax  
  
```  
  
      catch (bad_typeid)  
   statement  
```  
  
## Remarks  
 The interface for `bad_typeid` is:  
  
```  
class bad_typeid : public exception  
{  
public:  
   bad_typeid(const char * _Message = "bad typeid");  
   bad_typeid(const bad_typeid &);  
   virtual ~bad_typeid();  
};  
```  
  
 The following example shows the `typeid` operator throwing a `bad_typeid` exception.  
  
```  
// expre_bad_typeid.cpp  
// compile with: /EHsc /GR  
#include <typeinfo.h>  
#include <iostream>  
  
class A{  
public:  
   // object for class needs vtable  
   // for RTTI  
   virtual ~A();  
};  
  
using namespace std;  
int main() {  
A* a = NULL;  
  
try {  
   cout << typeid(*a).name() << endl;  // Error condition  
   }  
catch (bad_typeid){  
   cout << "Object is NULL" << endl;  
   }  
}  
```  
  
## Output  
  
```  
Object is NULL  
```  
  
## See Also  
 [Run-Time Type Information](../vs140/Run-Time-Type-Information.md)   
 [Keywords](../vs140/Keywords--C---.md)