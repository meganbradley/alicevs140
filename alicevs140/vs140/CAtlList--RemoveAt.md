---
title: "CAtlList::RemoveAt"
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
ms.assetid: 907771c1-59a5-4527-8a4c-62fa0ed034b1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::RemoveAt
Call this method to remove a single element from the list.  
  
## Syntax  
  
```  
  
      void RemoveAt(  
   POSITION pos   
) throw( );  
```  
  
#### Parameters  
 `pos`  
 The POSITION value of the element to remove.  
  
## Remarks  
 The element referenced by `pos` is removed, and memory is freed. It is acceptable to use `RemoveAt` to remove the head or tail of the list.  
  
 In debug builds, an assertion failure will occur if the list is not valid or if removing the element causes the list to access memory which isn't part of the list structure.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#27](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#27)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::RemoveAll](../vs140/CAtlList--RemoveAll.md)   
 [CAtlList::SetAt](../vs140/CAtlList--SetAt.md)