---
title: "CRBMap::SetAt"
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
ms.assetid: 9d7f9a93-6cda-4434-8514-30ba6e46dda7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBMap::SetAt
Call this method to insert an element pair into the map.  
  
## Syntax  
  
```  
  
      POSITION SetAt(  
   KINARGTYPE key,  
   VINARGTYPE value   
) throw(...);  
```  
  
#### Parameters  
 `key`  
 The key value to add to the `CRBMap` object.  
  
 *value*  
 The value to add to the `CRBMap` object.  
  
## Return Value  
 Returns the position of the key/value element pair in the `CRBMap` object.  
  
## Remarks  
 `SetAt` replaces an existing element if a matching key is found. If the key is not found, a new key/value pair is created.  
  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#84](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#84)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBMap Class](../vs140/CRBMap-Class.md)   
 [CRBMap::RemoveKey](../vs140/CRBMap--RemoveKey.md)