---
title: "RuntimeClassBaseT::AsIID Method"
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
ms.assetid: 90d7df8a-cf9e-4eef-8837-bc1a25f3fa1a
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RuntimeClassBaseT::AsIID Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
template<  
   typename T  
>  
__forceinline static HRESULT AsIID(  
   _In_ T* implements,  
   REFIID riid,  
   _Deref_out_ void **ppvObject  
);  
```  
  
#### Parameters  
 `T`  
 A type that implements the interface ID specified by parameter `riid`.  
  
 `implements`  
 A variable of the type specified by template parameter `T`.  
  
 `riid`  
 The interface ID to retrieve.  
  
 `ppvObject`  
 If this operation is successful, a pointer-to-a-pointer to the interface specified by parameter `riid`.  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that describes the error.  
  
## Remarks  
 Retrieves a pointer to the specified interface ID.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [RuntimeClassBaseT Structure](../vs140/RuntimeClassBaseT-Structure.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)