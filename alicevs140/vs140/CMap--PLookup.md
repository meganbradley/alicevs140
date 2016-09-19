---
title: "CMap::PLookup"
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
ms.assetid: 6e81903b-ecf6-429f-bb8e-ea97d4d8301c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::PLookup
Finds the value mapped to a given key.  
  
## Syntax  
  
```  
  
      const CPair* PLookup(  
   ARG_KEY key  
) const;  
CPair* PLookup(   
   ARG_KEY key   
);  
```  
  
#### Parameters  
 `key`  
 Key for the element to be searched for.  
  
## Return Value  
 A pointer to a key structure; see [CMap::CPair](../vs140/CMap--CPair.md). If no match is found, `CMap::PLookup` returns `NULL`.  
  
## Remarks  
 Call this method to search for a map element with a key that exactly matches the given key.  
  
## Example  
 [!CODE [NVC_MFCCollections#60](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#60)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMap::PGetNextAssoc](../vs140/CMap--PGetNextAssoc.md)   
 [CMap::PGetFirstAssoc](../vs140/CMap--PGetFirstAssoc.md)