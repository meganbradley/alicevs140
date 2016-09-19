---
title: "CHAIN_MSG_MAP_ALT_MEMBER"
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
ms.assetid: f0c130ec-52fa-4a76-9a2c-5c217aaaea1a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHAIN_MSG_MAP_ALT_MEMBER
Defines an entry in a message map.  
  
## Syntax  
  
```  
  
CHAIN_MSG_MAP_ALT_MEMBER( theChainMember, msgMapID )  
```  
  
#### Parameters  
 `theChainMember`  
 [in] The name of the data member containing the message map.  
  
 `msgMapID`  
 [in] The message map identifier.  
  
## Remarks  
 `CHAIN_MSG_MAP_ALT_MEMBER` directs messages to an alternate message map in a data member. You must have declared this alternate message map with [ALT_MSG_MAP(msgMapID)](../vs140/ALT_MSG_MAP.md). To direct messages to a data member's default message map (declared with [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md)), use `CHAIN_MSG_MAP_MEMBER`. For an example, see [CHAIN_MSG_MAP_MEMBER](../vs140/CHAIN_MSG_MAP_MEMBER.md).  
  
> [!NOTE]
>  Always begin a message map with `BEGIN_MSG_MAP`. You can then declare subsequent alternate message maps with `ALT_MSG_MAP`. The [END_MSG_MAP](../vs140/END_MSG_MAP.md) macro marks the end of the message map. Every message map must have exactly one instance of `BEGIN_MSG_MAP` and `END_MSG_MAP`.  
  
 For more information about using message maps in ATL, see [Message Maps](../vs140/Message-Maps--ATL-.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [CHAIN_MSG_MAP_ALT](../vs140/CHAIN_MSG_MAP_ALT.md)