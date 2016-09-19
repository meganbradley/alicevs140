---
title: "CComUnkArray::GetUnknown"
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
ms.assetid: cc921e9f-2d9d-4756-969a-51e740989039
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComUnkArray::GetUnknown
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
 [CComUnkArray Class](../vs140/CComUnkArray-Class.md)   
 [CComUnkArray::GetCookie](../vs140/CComUnkArray--GetCookie.md)