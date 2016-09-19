---
title: "CDynamicChain::RemoveChainEntry"
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
ms.assetid: 00bbbdc0-0af2-40b6-b1cd-6ca025e83273
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicChain::RemoveChainEntry
Removes the specified message map from the collection.  
  
## Syntax  
  
```  
  
      BOOL RemoveChainEntry(  
   DWORD dwChainID   
);  
```  
  
#### Parameters  
 `dwChainID`  
 [in] The unique identifier associated with the chained object and its message map. You originally define this value through a call to [SetChainEntry](../vs140/CDynamicChain--SetChainEntry.md).  
  
## Return Value  
 **TRUE** if the message map is successfully removed from the collection. Otherwise, **FALSE**.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CDynamicChain Class](../vs140/CDynamicChain-Class.md)