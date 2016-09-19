---
title: "CList::GetTail"
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
ms.assetid: 7aa81545-8a0d-4a20-8537-6ca2ecd3ef2a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::GetTail
Gets the `CObject` pointer that represents the tail element of this list.  
  
## Syntax  
  
```  
  
      TYPE  
      & GetTail( );  
const TYPE& GetTail() const;  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements in the list.  
  
## Return Value  
 See the return value description for [GetHead](../vs140/CObList--GetHead.md).  
  
## Remarks  
 You must ensure that the list is not empty before calling `GetTail`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CObList--IsEmpty.md) to verify that the list contains elements.  
  
## Example  
 [!CODE [NVC_MFCCollections#46](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#46)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::AddTail](../vs140/CList--AddTail.md)   
 [CList::AddHead](../vs140/CList--AddHead.md)   
 [CList::RemoveHead](../vs140/CList--RemoveHead.md)   
 [CList::GetHead](../vs140/CList--GetHead.md)