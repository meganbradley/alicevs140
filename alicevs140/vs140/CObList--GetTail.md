---
title: "CObList::GetTail"
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
ms.assetid: d49712f3-d7c7-4559-a73b-4577496c6c5b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::GetTail
Gets the `CObject` pointer that represents the tail element of this list.  
  
## Syntax  
  
```  
  
      CObject*& GetTail( );  
const CObject*& GetTail( ) const;  
```  
  
## Return Value  
 See the return value description for [GetHead](../vs140/CObList--GetHead.md).  
  
## Remarks  
 You must ensure that the list is not empty before calling `GetTail`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CObList--IsEmpty.md) to verify that the list contains elements.  
  
 The following table shows other member functions that are similar to `CObList::GetTail`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**const void\*& GetTail( ) const; void\*& GetTail( );**|  
|[CStringList](../vs140/CStringList-Class.md)|**const CString& GetTail( ) const; CString& GetTail( );**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#101](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#101)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::AddTail](../vs140/CObList--AddTail.md)   
 [CObList::AddHead](../vs140/CObList--AddHead.md)   
 [CObList::RemoveHead](../vs140/CObList--RemoveHead.md)   
 [CObList::GetHead](../vs140/CObList--GetHead.md)