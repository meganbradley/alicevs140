---
title: "CObArray::GetCount"
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
ms.assetid: f399ab7e-2976-4546-abc7-effb0ab1cf0f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::GetCount
Returns the number of array elements.  
  
## Syntax  
  
```  
  
INT_PTR GetCount( ) const;  
```  
  
## Return Value  
 The number of items in the array.  
  
## Remarks  
 Call this method to retrieve the number of elements in the array. Because indexes are zero-based, the size is 1 greater than the largest index.  
  
 The following table shows other member functions that are similar to `CObArray::GetCount`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**INT_PTR GetCount( ) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#80](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#80)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::GetUpperBound](../vs140/CObArray--GetUpperBound.md)   
 [CObArray::SetSize](../vs140/CObArray--SetSize.md)   
 [CObArray::GetSize](../vs140/CObArray--GetSize.md)