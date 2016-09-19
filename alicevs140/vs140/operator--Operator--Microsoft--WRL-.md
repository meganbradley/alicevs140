---
title: "operator&lt; Operator (Microsoft::WRL)"
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
ms.assetid: bfae0e1c-1648-482b-99c2-3217d62aba46
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&lt; Operator (Microsoft::WRL)
Determines if the address of one object is less than another.  
  
## Syntax  
  
```cpp  
template<class T, class U>  
bool operator<(const ComPtr<T>& a, const ComPtr<U>& b) throw();  
template<class T, class U>  
bool operator<(const Details::ComPtrRef<ComPtr<T>>& a, const Details::ComPtrRef<ComPtr<U>>& b) throw();  
```  
  
#### Parameters  
 `a`  
 The left object.  
  
 `b`  
 The right object.  
  
## Return Value  
 `true` if the address of `a` is less than the address of `b`; otherwise, `false`.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)