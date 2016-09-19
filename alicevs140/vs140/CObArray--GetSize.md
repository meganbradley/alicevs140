---
title: "CObArray::GetSize"
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
ms.assetid: 45b201a2-864a-4294-993c-e018788168e9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::GetSize
Returns the size of the array.  
  
## Syntax  
  
```  
  
INT_PTR GetSize( ) const;  
```  
  
## Remarks  
 Since indexes are zero-based, the size is 1 greater than the largest index.  
  
 The following table shows other member functions that are similar to `CObArray::GetSize`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**INT_PTR GetSize( ) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#82](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#82)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::GetUpperBound](../vs140/CObArray--GetUpperBound.md)   
 [CObArray::SetSize](../vs140/CObArray--SetSize.md)   
 [CObArray::GetCount](../vs140/CObArray--GetCount.md)