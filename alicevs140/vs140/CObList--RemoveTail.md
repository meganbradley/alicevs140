---
title: "CObList::RemoveTail"
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
ms.assetid: cba5b5a3-1b6d-4c4e-af60-0074049705d3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::RemoveTail
Removes the element from the tail of the list and returns a pointer to it.  
  
## Syntax  
  
```  
  
CObject* RemoveTail( );  
```  
  
## Return Value  
 A pointer to the object that was at the tail of the list.  
  
## Remarks  
 You must ensure that the list is not empty before calling `RemoveTail`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CObList--IsEmpty.md) to verify that the list contains elements.  
  
 The following table shows other member functions that are similar to `CObList::RemoveTail`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**void\* RemoveTail( );**|  
|[CStringList](../vs140/CStringList-Class.md)|**CString RemoveTail( );**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#108](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#108)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::GetTail](../vs140/CObList--GetTail.md)   
 [CObList::AddTail](../vs140/CObList--AddTail.md)