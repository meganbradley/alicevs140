---
title: "CMapStringToString::PLookup"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 2b89bbcb-0d8e-4b60-b31a-4e786cec3f43
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToString::PLookup
Looks up the value mapped to a given key.  
  
## Syntax  
  
```  
const CPair* PLookup(  
   LPCTSTR key  
) const;  
CPair* PLookup(  
   LPCTSTR key  
);  
```  
  
#### Parameters  
 `key`  
 A pointer to the key for the element to be searched for.  
  
## Return Value  
 A pointer to the specified key.  
  
## Remarks  
 Call this method to search for a map element with a key that exactly matches the given key.  
  
## Example  
 [!CODE [NVC_MFCCollections#74](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#74)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToString Class](../vs140/CMapStringToString-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToString::PGetNextAssoc](../vs140/CMapStringToString--PGetNextAssoc.md)   
 [CMapStringToString::PGetFirstAssoc](../vs140/CMapStringToString--PGetFirstAssoc.md)