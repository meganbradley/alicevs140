---
title: "ActivateInstance Function"
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
ms.assetid: 8cfd1dd9-5fda-4cc2-acf8-d40e783b3875
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ActivateInstance Function
Registers and retrieves an instance of a specified type defined in a specified class ID.  
  
## Syntax  
  
```  
template<  
   typename T  
>  
inline HRESULT ActivateInstance(  
   _In_ HSTRING activatableClassId,  
   _Out_ Microsoft::WRL::Details::ComPtrRef<T> instance  
);  
```  
  
#### Parameters  
 `T`  
 A type to activate.  
  
 `activatableClassId`  
 The name of the class ID that defines parameter `T`.  
  
 `instance`  
 When this operation completes, a reference to an instance of `T`.  
  
## Return Value  
 S_OK if successful; otherwise, an error HRESULT that indicates the cause of the error.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Windows::Foundation  
  
## See Also  
 [Foundation Namespace](../vs140/Windows--Foundation-Namespace.md)