---
title: "CObList::RemoveHead"
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
ms.assetid: e19830dc-4bd3-48f4-8bf0-851e5ebcd245
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::RemoveHead
Removes the element from the head of the list and returns a pointer to it.  
  
## Syntax  
  
```  
  
CObject* RemoveHead( );  
```  
  
## Return Value  
 The `CObject` pointer previously at the head of the list.  
  
## Remarks  
 You must ensure that the list is not empty before calling `RemoveHead`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CObList--IsEmpty.md) to verify that the list contains elements.  
  
 The following table shows other member functions that are similar to `CObList::RemoveHead`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**void\* RemoveHead( );**|  
|[CStringList](../vs140/CStringList-Class.md)|**CString RemoveHead( );**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#107](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#107)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::GetHead](../vs140/CObList--GetHead.md)   
 [CObList::AddHead](../vs140/CObList--AddHead.md)