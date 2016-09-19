---
title: "CMapStringToString::PGetFirstAssoc"
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
ms.assetid: e2658177-5858-42e9-b0c6-10fc580716b2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToString::PGetFirstAssoc
Returns the first entry of the map object.  
  
## Syntax  
  
```  
const CPair* PGetFirstAssoc( ) const;   
CPair* PGetFirstAssoc( );  
```  
  
## Return Value  
 A pointer to the first entry in the map; see [CMapStringToString::CPair](../vs140/CMapStringToString--CPair.md). If the map is empty, the value is `NULL`.  
  
## Remarks  
 Call this function to return a pointer the first element in the map object.  
  
## Example  
 [!CODE [NVC_MFCCollections#73](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#73)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToString Class](../vs140/CMapStringToString-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToString::PGetNextAssoc](../vs140/CMapStringToString--PGetNextAssoc.md)   
 [CMapStringToString::PLookup](../vs140/CMapStringToString--PLookup.md)