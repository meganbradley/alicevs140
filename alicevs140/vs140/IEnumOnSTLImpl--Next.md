---
title: "IEnumOnSTLImpl::Next"
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
ms.assetid: 3b3c92aa-ecb5-42c7-bf87-2552e3a9c8e4
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IEnumOnSTLImpl::Next
This method provides the implementation of the [IEnumXXXX::Next](https://msdn.microsoft.com/en-us/library/ms695273.aspx) method.  
  
## Syntax  
  
```  
  
      STDMETHOD(Next)(  
   ULONG celt,  
   T* rgelt,  
   ULONG* pceltFetched   
);  
```  
  
#### Parameters  
 `celt`  
 [in] The number of elements requested.  
  
 `rgelt`  
 [out] The array to be filled in with the elements.  
  
 `pceltFetched`  
 [out] The number of elements actually returned in `rgelt`. This can be less than `celt` if fewer than `celt` elements remain in the list.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IEnumOnSTLImpl Class](../vs140/IEnumOnSTLImpl-Class.md)