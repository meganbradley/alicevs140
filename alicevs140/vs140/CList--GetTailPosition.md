---
title: "CList::GetTailPosition"
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
ms.assetid: c464b7ee-5d58-4cf5-9fec-11a1a419a8af
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::GetTailPosition
Gets the position of the tail element of this list; **NULL** if the list is empty.  
  
## Syntax  
  
```  
  
POSITION GetTailPosition( ) const;  
```  
  
## Return Value  
 A **POSITION** value that can be used for iteration or object pointer retrieval; **NULL** if the list is empty.  
  
## Example  
 [!CODE [NVC_MFCCollections#47](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#47)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::GetHeadPosition](../vs140/CList--GetHeadPosition.md)   
 [CList::GetTail](../vs140/CList--GetTail.md)