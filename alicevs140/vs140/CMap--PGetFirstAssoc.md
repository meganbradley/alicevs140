---
title: "CMap::PGetFirstAssoc"
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
ms.assetid: 7bbe86e2-f61b-4f51-b837-f4dfa536e09a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::PGetFirstAssoc
Returns the first entry of the map object.  
  
## Syntax  
  
```  
  
      const CPair* PGetFirstAssoc( ) const;   
CPair* PGetFirstAssoc( );  
```  
  
## Return Value  
 A pointer to the first entry in the map; see [CMap::CPair](../vs140/CMap--CPair.md). If the map contains no entries, the value is **NULL**.  
  
## Remarks  
 Call this function to return a pointer the first element in the map object.  
  
## Example  
 [!CODE [NVC_MFCCollections#59](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#59)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMap::PGetNextAssoc](../vs140/CMap--PGetNextAssoc.md)   
 [CMap::PLookup](../vs140/CMap--PLookup.md)