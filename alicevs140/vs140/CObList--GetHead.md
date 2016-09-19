---
title: "CObList::GetHead"
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
ms.assetid: 17e320ed-6e17-4e0b-a4ca-17568585e576
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::GetHead
Gets the `CObject` pointer that represents the head element of this list.  
  
## Syntax  
  
```  
  
      CObject*& GetHead( );  
const CObject*& GetHead( ) const;  
```  
  
## Return Value  
 If the list is accessed through a pointer to a **const CObList**, then `GetHead` returns a `CObject` pointer. This allows the function to be used only on the right side of an assignment statement and thus protects the list from modification.  
  
 If the list is accessed directly or through a pointer to a `CObList`, then `GetHead` returns a reference to a `CObject` pointer. This allows the function to be used on either side of an assignment statement and thus allows the list entries to be modified.  
  
## Remarks  
 You must ensure that the list is not empty before calling `GetHead`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CObList--IsEmpty.md) to verify that the list contains elements.  
  
 The following table shows other member functions that are similar to `CObList::GetHead`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**const void\*& GetHead( ) const; void\*& GetHead( );**|  
|[CStringList](../vs140/CStringList-Class.md)|**const CString& GetHead( ) const; CString& GetHead( );**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 The following example illustrates the use of `GetHead` on the left side of an assignment statement.  
  
 [!CODE [NVC_MFCCollections#96](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#96)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::GetTail](../vs140/CObList--GetTail.md)   
 [CObList::GetTailPosition](../vs140/CObList--GetTailPosition.md)   
 [CObList::AddHead](../vs140/CObList--AddHead.md)   
 [CObList::RemoveHead](../vs140/CObList--RemoveHead.md)