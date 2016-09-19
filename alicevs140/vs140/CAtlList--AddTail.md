---
title: "CAtlList::AddTail"
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
ms.assetid: cc36cb17-00f2-4927-8a93-596b557fa383
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::AddTail
Call this method to add an element to the tail of this list.  
  
## Syntax  
  
```  
  
      POSITION AddTail( );   
POSITION AddTail(  
   INARGTYPE element   
);  
```  
  
#### Parameters  
 `element`  
 The element to add.  
  
## Return Value  
 Returns the POSITION of the newly added element.  
  
## Remarks  
 If the first version is used, an empty element is created using its default constructor, rather than its copy constructor. The element is added to the end of the list, and so it now becomes the tail. This method can be used with an empty list.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#15](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#15)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::AddTailList](../vs140/CAtlList--AddTailList.md)   
 [CAtlList::AddHead](../vs140/CAtlList--AddHead.md)