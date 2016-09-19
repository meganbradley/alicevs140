---
title: "CMapStringToString::PGetNextAssoc"
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
ms.assetid: f516fe14-171a-40f5-8296-22987e9f2fa3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToString::PGetNextAssoc
Retrieves the map element pointed to by `pAssocRec`.  
  
## Syntax  
  
```  
  
      const CPair *PGetNextAssoc(  
   const CPair* pAssoc  
) const;  
CPair *PGetNextAssoc(  
   const CPair* pAssoc  
);  
```  
  
#### Parameters  
 *pAssoc*  
 Points to a map entry returned by a previous [PGetNextAssoc](#vclrfcmapstringtostringpgetnextassoc) or [PGetFirstAssoc](../vs140/CMapStringToString--PGetFirstAssoc.md) call.  
  
## Return Value  
 A pointer to the next entry in the map; see [CMapStringToString::CPair](../vs140/CMapStringToString--CPair.md). If the element is the last in the map, the value is **NULL**.  
  
## Remarks  
 Call this method to iterate through all the elements in the map. Retrieve the first element with a call to `PGetFirstAssoc` and then iterate through the map with successive calls to `PGetNextAssoc`.  
  
## Example  
 See the example for [CMapStringToString::PGetFirstAssoc](../vs140/CMapStringToString--PGetFirstAssoc.md).  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToString Class](../vs140/CMapStringToString-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToString::PGetFirstAssoc](../vs140/CMapStringToString--PGetFirstAssoc.md)   
 [CMapStringToString::PLookup](../vs140/CMapStringToString--PLookup.md)