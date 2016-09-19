---
title: "CList::RemoveHead"
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
ms.assetid: 4c9aafaa-fff5-4cf5-b951-7bef5fd2caef
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::RemoveHead
Removes the element from the head of the list and returns a pointer to it.  
  
## Syntax  
  
```  
  
TYPE RemoveHead( );  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements in the list.  
  
## Return Value  
 The element previously at the head of the list.  
  
## Remarks  
 You must ensure that the list is not empty before calling `RemoveHead`. If the list is empty, then the Debug version of the Microsoft Foundation Class Library asserts. Use [IsEmpty](../vs140/CList--IsEmpty.md) to verify that the list contains elements.  
  
## Example  
 [!CODE [NVC_MFCCollections#53](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#53)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::GetHead](../vs140/CList--GetHead.md)   
 [CList::AddHead](../vs140/CList--AddHead.md)