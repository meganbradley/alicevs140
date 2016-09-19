---
title: "CHAIN_MSG_MAP_ALT"
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
ms.assetid: a181f51e-481d-4edb-984a-c710ac6a8bbb
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHAIN_MSG_MAP_ALT
Defines an entry in a message map.  
  
## Syntax  
  
```  
  
CHAIN_MSG_MAP_ALT( theChainClass, msgMapID )  
```  
  
#### Parameters  
 `theChainClass`  
 [in] The name of the base class containing the message map.  
  
 `msgMapID`  
 [in] The message map identifier.  
  
## Remarks  
 `CHAIN_MSG_MAP_ALT` directs messages to an alternate message map in a base class. You must have declared this alternate message map with [ALT_MSG_MAP(msgMapID)](../vs140/ALT_MSG_MAP.md). To direct messages to a base class's default message map (declared with [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md)), use `CHAIN_MSG_MAP`. For an example, see [CHAIN_MSG_MAP](../vs140/CHAIN_MSG_MAP.md).  
  
> [!NOTE]
>  Always begin a message map with `BEGIN_MSG_MAP`. You can then declare subsequent alternate message maps with `ALT_MSG_MAP`. The [END_MSG_MAP](../vs140/END_MSG_MAP.md) macro marks the end of the message map. Every message map must have exactly one instance of `BEGIN_MSG_MAP` and `END_MSG_MAP`.  
  
 For more information about using message maps in ATL, see [Message Maps](../vs140/Message-Maps--ATL-.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [CHAIN_MSG_MAP_ALT_MEMBER](../vs140/CHAIN_MSG_MAP_ALT_MEMBER.md)