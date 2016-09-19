---
title: "CRBMap::RemoveKey"
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
ms.assetid: 1cdc2f65-541a-4d54-a2b6-873df1f815aa
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBMap::RemoveKey
Call this method to remove an element from the `CRBMap` object, given the key.  
  
## Syntax  
  
```  
  
      bool RemoveKey(  
   KINARGTYPE key   
) throw( );  
```  
  
#### Parameters  
 `key`  
 The key corresponding to the element pair you want to remove.  
  
## Return Value  
 Returns true if the key is found and removed, false on failure.  
  
## Remarks  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#83](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#83)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBMap Class](../vs140/CRBMap-Class.md)   
 [CRBMap::SetAt](../vs140/CRBMap--SetAt.md)