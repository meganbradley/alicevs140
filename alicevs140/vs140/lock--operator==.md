---
title: "lock::operator=="
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
ms.assetid: 3dcf1e5a-53fc-495d-9df5-d7849a41c36c
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# lock::operator==
Equality operator.  
  
## Syntax  
  
```  
template<class T> bool operator==(  
   T t  
);  
```  
  
#### Parameters  
 `t`  
 The object to compare for equality.  
  
## Return Value  
 Returns `true` if `t` is the same as the lock's object, `false` otherwise.  
  
## Example  
  
```  
// msl_lock_op_eq.cpp  
// compile with: /clr  
#include <msclr/lock.h>  
  
using namespace System;  
using namespace System::Threading;  
using namespace msclr;  
  
int main () {  
   Object^ o1 = gcnew Object;  
   lock l1(o1);  
   if (l1 == o1) {  
      Console::WriteLine("Equal!");  
   }  
}  
```  
  
 **Equal!**   
## Requirements  
 **Header file** <msclr\lock.h>  
  
 **Namespace** msclr  
  
## See Also  
 [lock Members](../vs140/lock-Members.md)   
 [lock::operator!=](../vs140/lock--operator!=.md)