---
title: "CObArray::GetUpperBound"
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
ms.assetid: 89c486ea-fbaf-4d07-b29b-2953e1a1f2d6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::GetUpperBound
Returns the current upper bound of this array.  
  
## Syntax  
  
```  
  
INT_PTR GetUpperBound( ) const;  
```  
  
## Return Value  
 The index of the upper bound (zero-based).  
  
## Remarks  
 Because array indexes are zero-based, this function returns a value 1 less than `GetSize`.  
  
 The condition **GetUpperBound( )** = –1 indicates that the array contains no elements.  
  
 The following table shows other member functions that are similar to `CObArray::GetUpperBound`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**INT_PTR GetUpperBound( ) const;**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**INT_PTR GetUpperBound( ) const;**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**INT_PTR GetUpperBound( ) const;**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**INT_PTR GetUpperBound( ) const;**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**INT_PTR GetUpperBound( ) const;**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**INT_PTR GetUpperBound( ) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#83](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#83)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::GetSize](../vs140/CObArray--GetSize.md)   
 [CObArray::SetSize](../vs140/CObArray--SetSize.md)