---
title: "CMap::RemoveAll"
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
ms.assetid: 285b18f8-b843-4a35-925a-be8100dd625e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::RemoveAll
Removes all the values from this map by calling the global helper function **DestructElements**.  
  
## Syntax  
  
```  
  
void RemoveAll( );  
```  
  
## Remarks  
 The function works correctly if the map is already empty.  
  
## Example  
 [!CODE [NVC_MFCCollections#61](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#61)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMap::RemoveKey](../vs140/CMap--RemoveKey.md)