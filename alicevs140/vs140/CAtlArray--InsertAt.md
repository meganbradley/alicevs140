---
title: "CAtlArray::InsertAt"
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
ms.assetid: b4da3da0-a84e-4e50-a749-1104af7253cd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::InsertAt
Call this method to insert a new element (or multiple copies of an element) into the array object.  
  
## Syntax  
  
```  
  
      void InsertAt(  
   size_t iElement,  
   INARGTYPE element,  
   size_t nCount = 1   
);  
```  
  
#### Parameters  
 `iElement`  
 The index where the element or elements are to be inserted.  
  
 `element`  
 The value of the element or elements to be inserted.  
  
 `nCount`  
 The number of elements to add.  
  
## Remarks  
 Inserts one or more elements into the array, starting at index `iElement`. Existing elements are moved to avoid being overwritten.  
  
 In debug builds, an ATLASSERT will be raised if the `CAtlArray` object is invalid, the number of elements to be added is zero, or the combined number of elements is too large for the array to contain. In retail builds, passing invalid parameters may cause unpredictable results.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#9](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#9)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::Add](../vs140/CAtlArray--Add.md)