---
title: "CList::SetAt"
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
ms.assetid: 3b0554e6-0bcc-42f9-ba13-56603899143b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::SetAt
A variable of type **POSITION** is a key for the list.  
  
## Syntax  
  
```  
  
      void SetAt(  
   POSITION pos,  
   ARG_TYPE newElement   
);  
```  
  
#### Parameters  
 `pos`  
 The **POSITION** of the element to be set.  
  
 `ARG_TYPE`  
 Template parameter specifying the type of the list element (can be a reference).  
  
 `newElement`  
 The element to be added to the list.  
  
## Remarks  
 It is not the same as an index, and you cannot operate on a **POSITION** value yourself. `SetAt` writes the element to the specified position in the list.  
  
 You must ensure that your **POSITION** value represents a valid position in the list. If it is invalid, then the Debug version of the Microsoft Foundation Class Library asserts.  
  
## Example  
 [!CODE [NVC_MFCCollections#55](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#55)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::Find](../vs140/CList--Find.md)   
 [CList::GetAt](../vs140/CList--GetAt.md)   
 [CList::GetNext](../vs140/CList--GetNext.md)   
 [CList::GetPrev](../vs140/CList--GetPrev.md)