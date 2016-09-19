---
title: "CHAIN_MSG_MAP_DYNAMIC"
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
ms.assetid: 7e5c72b7-cb31-4f3b-8a1b-6293804af220
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHAIN_MSG_MAP_DYNAMIC
Defines an entry in a message map.  
  
## Syntax  
  
```  
  
CHAIN_MSG_MAP_DYNAMIC( dynaChainID )  
```  
  
#### Parameters  
 *dynaChainID*  
 [in] The unique identifier for an object's message map.  
  
## Remarks  
 `CHAIN_MSG_MAP_DYNAMIC` directs messages, at run time, to the default message map in another object. The object and its message map are associated with *dynaChainID*, which you define through [CDynamicChain::SetChainEntry](../vs140/CDynamicChain--SetChainEntry.md). You must derive your class from `CDynamicChain` in order to use `CHAIN_MSG_MAP_DYNAMIC`. For an example, see the [CDynamicChain](../vs140/CDynamicChain-Class.md) overview.  
  
> [!NOTE]
>  Always begin a message map with [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md). You can then declare subsequent alternate message maps with `ALT_MSG_MAP`. The [END_MSG_MAP](../vs140/END_MSG_MAP.md) macro marks the end of the message map. Every message map must have exactly one instance of `BEGIN_MSG_MAP` and `END_MSG_MAP`.  
  
 For more information about using message maps in ATL, see [Message Maps](../vs140/Message-Maps--ATL-.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [CHAIN_MSG_MAP](../vs140/CHAIN_MSG_MAP.md)   
 [CHAIN_MSG_MAP_MEMBER](../vs140/CHAIN_MSG_MAP_MEMBER.md)