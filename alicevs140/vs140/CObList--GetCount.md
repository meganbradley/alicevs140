---
title: "CObList::GetCount"
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
ms.assetid: 81fd15f6-9bf1-4930-86fc-b8bf264ae561
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::GetCount
Gets the number of elements in this list.  
  
## Syntax  
  
```  
  
INT_PTR GetCount( ) const;  
```  
  
## Return Value  
 An integer value containing the element count.  
  
 The following table shows other member functions that are similar to `CObList::GetCount`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**INT_PTR GetCount( ) const;**|  
|[CStringList](../vs140/CStringList-Class.md)|**INT_PTR GetCount( ) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#95](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#95)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::IsEmpty](../vs140/CObList--IsEmpty.md)