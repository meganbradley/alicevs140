---
title: "CList::GetHead"
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
ms.assetid: ff088b08-3d79-4753-a855-369388560452
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::GetHead
Gets the head element (or a reference to the head element) of this list.  
  
## Syntax  
  
```  
  
      const   
      TYPE  
      & GetHead( ) const;  
TYPE& GetHead( );  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of object in the list.  
  
## Return Value  
 If the list is **const**, `GetHead` returns a copy of the element at the head of the list. This allows the function to be used only on the right side of an assignment statement and protects the list from modification.  
  
 If the list is not **const**, `GetHead` returns a reference to the element at the head of the list. This allows the function to be used on either side of an assignment statement and thus allows the list entries to be modified.  
  
## Remarks  
 You must ensure that the list is not empty before calling `GetHead`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CList--IsEmpty.md) to verify that the list contains elements.  
  
## Example  
 [!CODE [NVC_MFCCollections#41](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#41)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::GetTail](../vs140/CList--GetTail.md)   
 [CList::GetTailPosition](../vs140/CList--GetTailPosition.md)   
 [CList::AddHead](../vs140/CList--AddHead.md)   
 [CList::RemoveHead](../vs140/CList--RemoveHead.md)