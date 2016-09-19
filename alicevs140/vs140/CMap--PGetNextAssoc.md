---
title: "CMap::PGetNextAssoc"
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
ms.assetid: 05659586-3aeb-4740-9ea7-40f2bf754dd3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::PGetNextAssoc
Retrieves the map element pointed to by `pAssocRec`.  
  
## Syntax  
  
```  
  
      const CPair *PGetNextAssoc(  
   const CPair* pAssocRet  
) const;  
CPair *PGetNextAssoc(  
   const CPair* pAssocRet  
);  
```  
  
#### Parameters  
 *pAssocRet*  
 Points to a map entry returned by a previous [PGetNextAssoc](#vclrfcmappgetnextassoc) or [CMap::PGetFirstAssoc](../vs140/CMap--PGetFirstAssoc.md) call.  
  
## Return Value  
 A pointer to the next entry in the map; see [CMap::CPair](../vs140/CMap--CPair.md). If the element is the last in the map, the value is **NULL**.  
  
## Remarks  
 Call this method to iterate through all the elements in the map. Retrieve the first element with a call to `PGetFirstAssoc` and then iterate through the map with successive calls to `PGetNextAssoc`.  
  
## Example  
 See the example for [CMap::PGetFirstAssoc](../vs140/CMap--PGetFirstAssoc.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMap::PGetFirstAssoc](../vs140/CMap--PGetFirstAssoc.md)   
 [CMap::PLookup](../vs140/CMap--PLookup.md)