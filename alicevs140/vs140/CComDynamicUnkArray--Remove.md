---
title: "CComDynamicUnkArray::Remove"
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
ms.assetid: a8538d3d-29a6-4b83-98d1-85cecb65a890
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComDynamicUnkArray::Remove
Call this method to remove an **IUnknown** pointer from the array.  
  
## Syntax  
  
```  
  
      BOOL Remove(  
   DWORD dwCookie   
);  
```  
  
#### Parameters  
 `dwCookie`  
 The cookie referencing the **IUnknown** pointer to be removed from the array.  
  
## Return Value  
 Returns TRUE if the pointer is removed; otherwise FALSE.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComDynamicUnkArray Class](../vs140/CComDynamicUnkArray-Class.md)   
 [CComDynamicUnkArray::Add](../vs140/CComDynamicUnkArray--Add.md)   
 [CComDynamicUnkArray::GetCookie](../vs140/CComDynamicUnkArray--GetCookie.md)