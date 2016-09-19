---
title: "CAtlArray::Add"
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
ms.assetid: 2db1f70a-7a9c-4560-aec7-12dcc6396f9e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::Add
Call this method to add an element to the array object.  
  
## Syntax  
  
```  
  
      size_t Add(  
   INARGTYPE element   
);  
size_t Add( );  
```  
  
#### Parameters  
 `element`  
 The element to be added to the array.  
  
## Return Value  
 Returns the index of the added element.  
  
## Remarks  
 The new element is added to the end of the array. If no element is provided, an empty element is added; that is, the array is increased in size as though a real element has been added. If the operation fails, [AtlThrow](../vs140/AtlThrow.md) is called with the argument E_OUTOFMEMORY.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#1](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#1)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::InsertAt](../vs140/CAtlArray--InsertAt.md)