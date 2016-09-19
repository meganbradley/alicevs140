---
title: "CObList::Find"
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
ms.assetid: 3e13fff4-6062-4fb8-9b04-9e9b06f7429d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::Find
Searches the list sequentially to find the first `CObject` pointer matching the specified `CObject` pointer.  
  
## Syntax  
  
```  
  
      POSITION Find(  
   CObject* searchValue,  
   POSITION startAfter = NULL   
) const;  
```  
  
#### Parameters  
 `searchValue`  
 The object pointer to be found in this list.  
  
 `startAfter`  
 The start position for the search.  
  
## Return Value  
 A **POSITION** value that can be used for iteration or object pointer retrieval; **NULL** if the object is not found.  
  
## Remarks  
 Note that the pointer values are compared, not the contents of the objects.  
  
 The following table shows other member functions that are similar to `CObList::Find`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**POSITION Find( void\***  `searchValue` **, POSITION**  `startAfter`  **= NULL ) const;**|  
|[CStringList](../vs140/CStringList-Class.md)|**POSITION Find( LPCTSTR**  `searchValue` **, POSITION**  `startAfter`  **= NULL ) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#93](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#93)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::GetNext](../vs140/CObList--GetNext.md)   
 [CObList::GetPrev](../vs140/CObList--GetPrev.md)