---
title: "CAtlList::AddHeadList"
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
ms.assetid: 36499b62-279d-4ecb-a342-94e28b71e6b6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::AddHeadList
Call this method to add an existing list to the head of the list.  
  
## Syntax  
  
```  
  
      void AddHeadList(  
   const CAtlList< E, ETraits >* plNew   
);  
```  
  
#### Parameters  
 `plNew`  
 The list to be added.  
  
## Remarks  
 The list pointed to by `plNew` is inserted at the start of the existing list. In debug builds, an assertion failure will occur if `plNew` is equal to NULL.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#14](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#14)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::AddHead](../vs140/CAtlList--AddHead.md)   
 [CAtlList::AddTailList](../vs140/CAtlList--AddTailList.md)