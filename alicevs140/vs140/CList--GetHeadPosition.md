---
title: "CList::GetHeadPosition"
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
ms.assetid: a8b56474-4709-4059-8245-06ee2626f274
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::GetHeadPosition
Gets the position of the head element of this list.  
  
## Syntax  
  
```  
  
POSITION GetHeadPosition( ) const;  
```  
  
## Return Value  
 A **POSITION** value that can be used for iteration or object pointer retrieval; **NULL** if the list is empty.  
  
## Example  
 [!CODE [NVC_MFCCollections#42](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#42)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::GetTailPosition](../vs140/CList--GetTailPosition.md)