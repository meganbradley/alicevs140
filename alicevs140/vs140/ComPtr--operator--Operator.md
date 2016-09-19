---
title: "ComPtr::operator&amp; Operator"
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
ms.topic: reference
ms.assetid: 2d77fda6-f4b2-45c1-8a0e-fbc355013531
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtr::operator&amp; Operator
Releases the interface associated with this `ComPtr` object and then retrieves the address of the `ComPtr` object.  
  
## Syntax  
  
```cpp  
Details::ComPtrRef<WeakRef> operator&()  
  
const Details::ComPtrRef<const WeakRef> operator&() const  
```  
  
## Return Value  
 A weak reference to the current `ComPtr`.  
  
## Remarks  
 This method differs from [ComPtr::GetAddressOf](../vs140/ComPtr--GetAddressOf-Method.md) in that this method releases a reference to the interface pointer. Use `ComPtr::GetAddressOf` when you require the address of the interface pointer but do not want to release that interface.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ComPtr Class](../vs140/ComPtr-Class.md)