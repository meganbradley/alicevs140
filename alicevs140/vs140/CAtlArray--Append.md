---
title: "CAtlArray::Append"
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
ms.assetid: 5d02ac66-b740-4629-926b-15eb4969108e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::Append
Call this method to add the contents of one array to the end of another.  
  
## Syntax  
  
```  
  
      size_t Append(  
   const CAtlArray< E, ETraits >& aSrc   
);  
```  
  
#### Parameters  
 `aSrc`  
 The array to append.  
  
## Return Value  
 Returns the index of the first appended element.  
  
## Remarks  
 The elements in the supplied array are added to the end of the existing array. If necessary, memory will be allocated to accommodate the new elements.  
  
 The arrays must be of the same type, and it is not possible to append an array to itself.  
  
 In debug builds, an ATLASSERT will be raised if the `CAtlArray` argument is not a valid array or if `aSrc` refers to the same object. In release builds, invalid arguments may lead to unpredictable behavior.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#2](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#2)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::InsertArrayAt](../vs140/CAtlArray--InsertArrayAt.md)