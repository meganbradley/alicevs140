---
title: "CComUnkArray::Remove"
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
ms.assetid: 017bb3e7-c9ba-44cb-a570-fc306140fe96
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComUnkArray::Remove
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
 Returns **TRUE** if the pointer is removed, **FALSE** otherwise.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComUnkArray Class](../vs140/CComUnkArray-Class.md)   
 [CComUnkArray::Add](../vs140/CComUnkArray--Add.md)