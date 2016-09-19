---
title: "ICollectionOnSTLImpl::get_Count"
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
ms.assetid: 4fa1bc3b-ed26-45f3-9f1a-8321ba03069f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICollectionOnSTLImpl::get_Count
This method returns the number of items in the collection.  
  
## Syntax  
  
```  
  
      STDMETHOD(get_Count)(  
   long* pcount   
);  
```  
  
#### Parameters  
 *pcount*  
 [out] The number of elements in the collection.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [ICollectionOnSTLImpl Class](../vs140/ICollectionOnSTLImpl-Class.md)