---
title: "CComDynamicUnkArray::GetUnknown"
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
ms.assetid: c1fad18b-43f7-4035-8f15-8658c595c0c0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComDynamicUnkArray::GetUnknown
Call this method to get the **IUnknown** pointer associated with a given cookie.  
  
## Syntax  
  
```  
  
      IUnknown* WINAPI GetUnknown(  
   DWORD dwCookie   
);  
```  
  
#### Parameters  
 `dwCookie`  
 The cookie for which the associated **IUnknown** pointer is required.  
  
## Return Value  
 Returns the **IUnknown** pointer, or NULL if no matching cookie is found.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComDynamicUnkArray Class](../vs140/CComDynamicUnkArray-Class.md)   
 [CComDynamicUnkArray::GetCookie](../vs140/CComDynamicUnkArray--GetCookie.md)