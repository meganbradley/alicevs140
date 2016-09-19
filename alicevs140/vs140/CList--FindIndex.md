---
title: "CList::FindIndex"
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
ms.assetid: c747e1d6-62bb-45a1-9a69-2714d153f00a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::FindIndex
Uses the value of `nIndex` as an index into the list.  
  
## Syntax  
  
```  
  
      POSITION FindIndex(  
   INT_PTR nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 The zero-based index of the list element to be found.  
  
## Return Value  
 A **POSITION** value that can be used for iteration or object pointer retrieval; **NULL** if `nIndex` is negative or too large.  
  
## Remarks  
 It starts a sequential scan from the head of the list, stopping on the *n*th element.  
  
## Example  
 [!CODE [NVC_MFCCollections#40](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#40)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::Find](../vs140/CObList--Find.md)   
 [CObList::GetNext](../vs140/CObList--GetNext.md)   
 [CObList::GetPrev](../vs140/CObList--GetPrev.md)