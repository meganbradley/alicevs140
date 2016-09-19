---
title: "CAtlList::SwapElements"
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
ms.assetid: e8d7e2dd-52f1-43f1-9a48-b882392af52e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::SwapElements
Call this method to swap elements in the list.  
  
## Syntax  
  
```  
  
      void SwapElements(  
   POSITION pos1,  
   POSITION pos2   
) throw( );  
```  
  
#### Parameters  
 *pos1*  
 The first POSITION value.  
  
 *pos2*  
 The second POSITION value.  
  
## Remarks  
 Swaps the elements at the two positions specified. In debug builds, an assertion failure will occur if either position value is equal to NULL.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#31](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#31)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::MoveToHead](../vs140/CAtlList--MoveToHead.md)   
 [CAtlList::MoveToTail](../vs140/CAtlList--MoveToTail.md)