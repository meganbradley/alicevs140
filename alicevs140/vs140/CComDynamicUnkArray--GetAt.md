---
title: "CComDynamicUnkArray::GetAt"
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
ms.assetid: e68a25ed-5cc0-4fd5-bcb0-b074413a2212
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComDynamicUnkArray::GetAt
Retrieves the element at the specified index.  
  
## Syntax  
  
```  
  
      IUnknown* GetAt(  
   int nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 The index of the element to retrieve.  
  
## Return Value  
 A pointer to an [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509) interface.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComDynamicUnkArray Class](../vs140/CComDynamicUnkArray-Class.md)