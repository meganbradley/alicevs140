---
title: "ComPtr::operator== Operator"
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
ms.assetid: 6a26e936-29d4-4b7d-b44a-7c575ad07509
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtr::operator== Operator
Indicates whether two ComPtr objects are equal.  
  
## Syntax  
  
```cpp  
bool operator==(  
   const ComPtr<T>& a,  
   const ComPtr<U>& b  
);  
  
bool operator==(  
   const ComPtr<T>& a,  
   decltype(__nullptr)  
);  
  
bool operator==(  
   decltype(__nullptr),  
   const ComPtr<T>& a  
);  
  
```  
  
#### Parameters  
 `a`  
 A reference to a ComPtr object.  
  
 `b`  
 A reference to another ComPtr object.  
  
## Return Value  
 The first operator yields `true` if object `a` is equal to object `b`; otherwise, `false`.  
  
 The second and third operators yield `true` if object `a` is equal to `nullptr`; otherwise, `false`.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)   
 [ComPtr Class](../vs140/ComPtr-Class.md)