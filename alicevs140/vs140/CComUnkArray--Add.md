---
title: "CComUnkArray::Add"
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
ms.assetid: 1dd5d4df-aeae-4c9a-8c74-171191ebac76
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComUnkArray::Add
Call this method to add an **IUnknown** pointer to the array.  
  
## Syntax  
  
```  
  
      DWORD Add(  
   IUnknown* pUnk   
);  
```  
  
#### Parameters  
 *pUnk*  
 Call this method to add an **IUnknown** pointer to the array.  
  
## Return Value  
 Returns the cookie associated with the newly added pointer, or 0 if the array is not large enough to contain the new pointer.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComUnkArray Class](../vs140/CComUnkArray-Class.md)   
 [CComUnkArray::Remove](../vs140/CComUnkArray--Remove.md)