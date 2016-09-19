---
title: "CAtlList::FindIndex"
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
ms.assetid: c298af99-07a8-450a-b280-b9b4673c7f03
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::FindIndex
Call this method to obtain the position of an element, given an index value.  
  
## Syntax  
  
```  
  
      POSITION FindIndex(  
   size_t iElement   
) const throw( );  
```  
  
#### Parameters  
 `iElement`  
 The zero-based index of the required list element.  
  
## Return Value  
 Returns the corresponding POSITION value, or NULL if `iElement` is out of range.  
  
## Remarks  
 This method returns the POSITION corresponding to a given index value, allowing access to the *n*th element in the list.  
  
 In debug builds, an assertion failure will occur if the list object is not valid.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#20](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#20)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::Find](../vs140/CAtlList--Find.md)