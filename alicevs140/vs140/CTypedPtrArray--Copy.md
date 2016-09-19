---
title: "CTypedPtrArray::Copy"
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
ms.assetid: 787307c8-1e86-4e8f-95f2-620071f0ea80
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrArray::Copy
This member function calls `BASE_CLASS`**::Copy**.  
  
## Syntax  
  
```  
  
      void Copy(  
   const CTypedPtrArray<BASE_CLASS,  
   TYPE>& src   
);  
```  
  
#### Parameters  
 `BASE_CLASS`  
 Base class of the typed pointer array class; must be an array class ([CObArray](../vs140/CObArray-Class.md) or [CPtrArray](../vs140/CPtrArray-Class.md)).  
  
 *TYPE*  
 Type of the elements stored in the base-class array.  
  
 *src*  
 Source of the elements to be copied to an array.  
  
## Remarks  
 For more detailed remarks, see [CObArray::Copy](../vs140/CObArray--Copy.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrArray Class](../vs140/CTypedPtrArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)