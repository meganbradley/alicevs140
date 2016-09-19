---
title: "CList::RemoveAt"
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
ms.assetid: 48f8b9b2-63fc-4d7e-8c2b-fbd4b5629082
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::RemoveAt
Removes the specified element from this list.  
  
## Syntax  
  
```  
  
      void RemoveAt(  
   POSITION position   
);  
```  
  
#### Parameters  
 *position*  
 The position of the element to be removed from the list.  
  
## Remarks  
 You must ensure that your **POSITION** value represents a valid position in the list. If it is invalid, then the Debug version of the Microsoft Foundation Class Library asserts.  
  
## Example  
 [!CODE [NVC_MFCCollections#52](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#52)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::RemoveAll](../vs140/CList--RemoveAll.md)