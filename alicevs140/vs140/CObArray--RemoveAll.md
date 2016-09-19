---
title: "CObArray::RemoveAll"
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
ms.assetid: 2e45ab17-92cd-4a42-9fc5-d0507a825617
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::RemoveAll
Removes all the pointers from this array but does not actually delete the `CObject` objects.  
  
## Syntax  
  
```  
  
void RemoveAll( );  
```  
  
## Remarks  
 If the array is already empty, the function still works.  
  
 The `RemoveAll` function frees all memory used for pointer storage.  
  
 The following table shows other member functions that are similar to `CObArray::RemoveAll`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**void RemoveAll( );**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**void RemoveAll( );**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**void RemoveAll( );**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**void RemoveAll( );**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**void RemoveAll( );**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**void RemoveAll( );**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#85](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#85)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)