---
title: "IEnumOnSTLImpl::Init"
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
ms.assetid: 5721fd59-97df-42bc-ac9f-5ce7cea96f39
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IEnumOnSTLImpl::Init
Initializes the enumerator.  
  
## Syntax  
  
```  
  
      HRESULT Init(  
   IUnknown* pUnkForRelease,  
   CollType& collection   
);  
```  
  
#### Parameters  
 `pUnkForRelease`  
 [in] The **IUnknown** pointer of an object that must be kept alive during the lifetime of the enumerator. Pass **NULL** if no such object exists.  
  
 `collection`  
 A reference to the STL container that holds the items to be enumerated.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 If you pass `Init` a reference to a collection held in another object, you can use the `pUnkForRelease` parameter to ensure that the object, and the collection it holds, is available for as long as the enumerator needs it.  
  
 You must call this method before passing a pointer to the enumerator interface back to any clients.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IEnumOnSTLImpl Class](../vs140/IEnumOnSTLImpl-Class.md)