---
title: "CRBMap::Lookup"
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
ms.assetid: e82722fc-aea4-46d1-90e5-d27b596b6c9a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBMap::Lookup
Call this method to look up keys or values in the `CRBMap` object.  
  
## Syntax  
  
```  
  
      bool Lookup(  
   KINARGTYPE key,  
   VOUTARGTYPE value   
) const throw(...);  
const CPair* Lookup(  
   KINARGTYPE key   
) const throw( );  
CPair* Lookup(  
   KINARGTYPE key   
) throw( );  
```  
  
#### Parameters  
 `key`  
 Specifies the key that identifies the element to be looked up.  
  
 *value*  
 Variable that receives the looked-up value.  
  
## Return Value  
 The first form of the method returns true if the key is found, otherwise false. The second and third forms return a pointer to a [CPair](../vs140/CRBTree--CPair-Class.md).  
  
## Remarks  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#82](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#82)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBMap Class](../vs140/CRBMap-Class.md)