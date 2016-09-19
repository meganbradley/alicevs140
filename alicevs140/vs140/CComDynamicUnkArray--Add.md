---
title: "CComDynamicUnkArray::Add"
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
ms.assetid: 29fc9e5e-ba08-4a91-9b84-b6877467a689
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComDynamicUnkArray::Add
Call this method to add an **IUnknown** pointer to the array.  
  
## Syntax  
  
```  
  
      DWORD Add(  
   IUnknown* pUnk   
);  
```  
  
#### Parameters  
 *pUnk*  
 The **IUnknown** pointer to add to the array.  
  
## Return Value  
 Returns the cookie associated with the newly added pointer.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComDynamicUnkArray Class](../vs140/CComDynamicUnkArray-Class.md)   
 [CComDynamicUnkArray::Remove](../vs140/CComDynamicUnkArray--Remove.md)