---
title: "ComPtr::GetAddressOf Method"
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
ms.assetid: 972a41d0-c2ef-4ae3-b2cd-77cc45156ac9
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtr::GetAddressOf Method
Retrieves the address of the [ptr_](../vs140/ComPtr--ptr_-Data-Member.md) data member, which contains a pointer to the interface represented by this ComPtr.  
  
## Syntax  
  
```  
T* const* GetAddressOf() const;  
T** GetAddressOf();  
```  
  
## Return Value  
 The address of a variable.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ComPtr Class](../vs140/ComPtr-Class.md)