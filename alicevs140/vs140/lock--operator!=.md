---
title: "lock::operator!="
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
ms.assetid: ed1d674e-9ee9-4257-8a7e-2e3567d50222
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# lock::operator!=
Inequality operator.  
  
## Syntax  
  
```  
template<class T> bool operator!=(  
   T t  
);  
```  
  
#### Parameters  
 `t`  
 The object to compare for inequality.  
  
## Return Value  
 Returns `true` if `t` differs from the lock's object, `false` otherwise.  
  
## Example  
  
```  
// msl_lock_op_ineq.cpp  
// compile with: /clr  
#include <msclr/lock.h>  
  
using namespace System;  
using namespace System::Threading;  
using namespace msclr;  
  
int main () {  
   Object^ o1 = gcnew Object;  
   Object^ o2 = gcnew Object;  
   lock l1(o1);  
   if (l1 != o2) {  
      Console::WriteLine("Inequal!");  
   }  
}  
```  
  
 **Inequal!**   
## Requirements  
 **Header file** <msclr\lock.h>  
  
 **Namespace** msclr  
  
## See Also  
 [lock Members](../vs140/lock-Members.md)   
 [lock::operator==](../vs140/lock--operator==.md)