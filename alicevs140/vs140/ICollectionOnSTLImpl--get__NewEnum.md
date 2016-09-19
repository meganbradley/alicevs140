---
title: "ICollectionOnSTLImpl::get__NewEnum"
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
ms.assetid: 936d1710-1f4c-46d4-a453-aba42e68444b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICollectionOnSTLImpl::get__NewEnum
Returns an enumerator object for the collection.  
  
## Syntax  
  
```  
  
      STDMETHOD(get__NewEnum)(  
   IUnknown** ppUnk   
);  
```  
  
#### Parameters  
 `ppUnk`  
 [out] The **IUnknown** pointer of a newly created enumerator object.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The newly created enumerator maintains an iterator on the original collection, `m_coll`, (so no copy is made) and holds a COM reference on the collection object to ensure that the collection remains alive while there are outstanding enumerators.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [ICollectionOnSTLImpl Class](../vs140/ICollectionOnSTLImpl-Class.md)   
 [Collections and Enumerators](../vs140/ATL-Collections-and-Enumerators.md)