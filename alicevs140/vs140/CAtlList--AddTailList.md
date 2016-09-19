---
title: "CAtlList::AddTailList"
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
ms.assetid: 9b98b3b5-896e-4abc-ad3a-3fc153cb01bb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::AddTailList
Call this method to add an existing list to the tail of this list.  
  
## Syntax  
  
```  
  
      void AddTailList(  
   const CAtlList< E, ETraits >* plNew   
);  
```  
  
#### Parameters  
 `plNew`  
 The list to be added.  
  
## Remarks  
 The list pointed to by `plNew` is inserted after the last element (if any) in the list object. The last element in the `plNew` list therefore becomes the tail. In debug builds, an assertion failure will occur if *plNew* is equal to NULL.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#16](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#16)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::AddTail](../vs140/CAtlList--AddTail.md)   
 [CAtlList::AddHead](../vs140/CAtlList--AddHead.md)