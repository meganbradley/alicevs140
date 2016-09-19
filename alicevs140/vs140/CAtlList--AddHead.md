---
title: "CAtlList::AddHead"
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
ms.assetid: 0854ebe8-50af-4c75-9705-30c876d7978a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::AddHead
Call this method to add an element to the head of the list.  
  
## Syntax  
  
```  
  
      POSITION AddHead( );   
POSITION AddHead(  
   INARGTYPE element   
);  
```  
  
#### Parameters  
 `element`  
 The new element.  
  
## Return Value  
 Returns the position of the newly added element.  
  
## Remarks  
 If the first version is used, an empty element is created using its default constructor, rather than its copy constructor.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#13](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#13)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::AddHeadList](../vs140/CAtlList--AddHeadList.md)   
 [CAtlList::AddTail](../vs140/CAtlList--AddTail.md)