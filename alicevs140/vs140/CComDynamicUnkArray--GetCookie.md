---
title: "CComDynamicUnkArray::GetCookie"
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
ms.assetid: 52779134-9f6e-4e11-b7ed-03b18bbb257b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComDynamicUnkArray::GetCookie
Call this method to get the cookie associated with a given **IUnknown** pointer.  
  
## Syntax  
  
```  
  
      DWORD WINAPI GetCookie(  
   IUnknown** ppFind   
);  
```  
  
#### Parameters  
 `ppFind`  
 The **IUnknown** pointer for which the associated cookie is required.  
  
## Return Value  
 Returns the cookie associated with the **IUnknown** pointer, or zero if no matching **IUnknown** pointer is found.  
  
## Remarks  
 If there is more than one instance of the same **IUnknown** pointer, this function returns the cookie for the first one.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComDynamicUnkArray Class](../vs140/CComDynamicUnkArray-Class.md)   
 [CComDynamicUnkArray::Add](../vs140/CComDynamicUnkArray--Add.md)   
 [CComDynamicUnkArray::Remove](../vs140/CComDynamicUnkArray--Remove.md)   
 [CComDynamicUnkArray::GetUnknown](../vs140/CComDynamicUnkArray--GetUnknown.md)