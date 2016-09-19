---
title: "CAtlList::SetAt"
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
ms.assetid: b0ad9dd9-d0f7-4adb-8fe5-d8af43f1442d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::SetAt
Call this method to set the value of the element at a given position in the list.  
  
## Syntax  
  
```  
  
      void SetAt(  
   POSITION pos,  
   INARGTYPE element   
);  
```  
  
#### Parameters  
 `pos`  
 The POSITION value corresponding to the element to change.  
  
 `element`  
 The new element value.  
  
## Remarks  
 Replaces the existing value with `element`. In debug builds, an assertion failure will occur if `pos` is equal to NULL.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#30](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#30)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::RemoveAt](../vs140/CAtlList--RemoveAt.md)