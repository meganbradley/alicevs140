---
title: "RuntimeClassBaseT::GetImplementedIIDS Method"
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
ms.assetid: adae54da-521d-4add-87f5-242fbd85f33b
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RuntimeClassBaseT::GetImplementedIIDS Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template<  
   typename T  
>  
__forceinline static HRESULT GetImplementedIIDS(  
   _In_ T* implements,  
   _Out_ ULONG *iidCount,  
   _Deref_out_ _Deref_post_cap_(*iidCount) IID **iids  
);  
```  
  
#### Parameters  
 `T`  
 The type of the `implements` parameter.  
  
 `implements`  
 Pointer to the type specified by parameter `T`.  
  
 `iidCount`  
 The maximum number of interface IDs to retrieve.  
  
 `iids`  
 If this operation completes successfully, an array of the interface IDs implemented by type `T`.  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that describes the error.  
  
## Remarks  
 Retrieves an array of interface IDs that are implemented by a specified type.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [RuntimeClassBaseT Structure](../vs140/RuntimeClassBaseT-Structure.md)