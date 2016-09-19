---
title: "IEnumOnSTLImpl::Clone"
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
ms.assetid: 6b87a9c4-6a0e-42cb-b4eb-03e32a793b4c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IEnumOnSTLImpl::Clone
This method provides the implementation of the [IEnumXXXX::Clone](https://msdn.microsoft.com/en-us/library/ms690336.aspx) method by creating an object of type `CComEnumOnSTL`, initializing it with the same collection and iterator used by the current object, and returning the interface on the newly created object.  
  
## Syntax  
  
```  
  
      STDMETHOD(Clone)(  
   Base** ppEnum   
);  
```  
  
#### Parameters  
 `ppEnum`  
 [out] The enumerator interface on a newly created object cloned from the current enumerator.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IEnumOnSTLImpl Class](../vs140/IEnumOnSTLImpl-Class.md)   
 [IEnumOnSTLImpl::Init](../vs140/IEnumOnSTLImpl--Init.md)