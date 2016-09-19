---
title: "ComPtr::ReleaseAndGetAddressOf Method"
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
ms.assetid: 3751dcb4-d50e-432c-89e4-e736be34d434
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtr::ReleaseAndGetAddressOf Method
Releases the interface associated with this ComPtr and then retrieves the address of the [ptr_](../vs140/ComPtr--ptr_-Data-Member.md) data member, which contains a pointer to the interface that was released.  
  
## Syntax  
  
```  
T** ReleaseAndGetAddressOf();  
```  
  
## Return Value  
 The address of the [ptr_](../vs140/ComPtr--ptr_-Data-Member.md) data member of this ComPtr.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ComPtr Class](../vs140/ComPtr-Class.md)   
 [ComPtr::ptr_ Data Member](../vs140/ComPtr--ptr_-Data-Member.md)