---
title: "CObList::GetHeadPosition"
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
ms.assetid: aeb3f0fb-9c1e-4a84-aeac-436f58ef1b7b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::GetHeadPosition
Gets the position of the head element of this list.  
  
## Syntax  
  
```  
  
POSITION GetHeadPosition( ) const;  
```  
  
## Return Value  
 A **POSITION** value that can be used for iteration or object pointer retrieval; **NULL** if the list is empty.  
  
 The following table shows other member functions that are similar to `CObList::GetHeadPosition`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**POSITION GetHeadPosition( ) const;**|  
|[CStringList](../vs140/CStringList-Class.md)|**POSITION GetHeadPosition( ) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#97](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#97)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::GetTailPosition](../vs140/CObList--GetTailPosition.md)