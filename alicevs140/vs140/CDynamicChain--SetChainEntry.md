---
title: "CDynamicChain::SetChainEntry"
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
ms.assetid: 712bde44-ee9b-4990-8bbf-3add4c47a9f0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicChain::SetChainEntry
Adds the specified message map to the collection.  
  
## Syntax  
  
```  
  
      BOOL SetChainEntry(  
   DWORD dwChainID,  
   CMessageMap* pObject,  
   DWORD dwMsgMapID = 0   
);  
```  
  
#### Parameters  
 `dwChainID`  
 [in] The unique identifier associated with the chained object and its message map.  
  
 `pObject`  
 [in] A pointer to the chained object declaring the message map. This object must derive from [CMessageMap](../vs140/CMessageMap-Class.md).  
  
 `dwMsgMapID`  
 [in] The identifier of the message map in the chained object. The default value is 0, which identifies the default message map declared with [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md). To specify an alternate message map declared with [ALT_MSG_MAP(msgMapID)](../vs140/ALT_MSG_MAP.md), pass `msgMapID`.  
  
## Return Value  
 **TRUE** if the message map is successfully added to the collection. Otherwise, **FALSE**.  
  
## Remarks  
 If the `dwChainID` value already exists in the collection, its associated object and message map are replaced by `pObject` and `dwMsgMapID`, respectively. Otherwise, a new entry is added.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CDynamicChain Class](../vs140/CDynamicChain-Class.md)   
 [CDynamicChain::CallChain](../vs140/CDynamicChain--CallChain.md)   
 [CDynamicChain::RemoveChainEntry](../vs140/CDynamicChain--RemoveChainEntry.md)   
 [CHAIN_MSG_MAP_DYNAMIC](../vs140/CHAIN_MSG_MAP_DYNAMIC.md)