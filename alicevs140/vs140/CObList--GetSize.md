---
title: "CObList::GetSize"
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
ms.assetid: e2cdbb42-5b5b-482c-8d7c-08b474bc5ec2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::GetSize
Returns the number of list elements.  
  
## Syntax  
  
```  
  
INT_PTR GetSize( ) const;  
```  
  
## Return Value  
 The number of items in the list.  
  
## Remarks  
 Call this method to retrieve the number of elements in the list.  
  
 The following table shows other member functions that are similar to `CObList::GetSize`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**INT_PTR GetSize( ) const;**|  
|[CStringList](../vs140/CStringList-Class.md)|**INT_PTR GetSize( ) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#100](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#100)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::GetCount](../vs140/CObList--GetCount.md)