---
title: "CHAIN_MSG_MAP_MEMBER"
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
ms.assetid: ac3e681c-2eb5-4f9b-9d89-2c5bc622523e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHAIN_MSG_MAP_MEMBER
Defines an entry in a message map.  
  
## Syntax  
  
```  
  
CHAIN_MSG_MAP_MEMBER( theChainMember )  
```  
  
#### Parameters  
 `theChainMember`  
 [in] The name of the data member containing the message map.  
  
## Remarks  
 `CHAIN_MSG_MAP_MEMBER` directs messages to a data member's default message map (declared with [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md)). To direct messages to a data member's alternate message map (declared with [ALT_MSG_MAP](../vs140/ALT_MSG_MAP.md)), use [CHAIN_MSG_MAP_ALT_MEMBER](../vs140/CHAIN_MSG_MAP_ALT_MEMBER.md).  
  
> [!NOTE]
>  Always begin a message map with `BEGIN_MSG_MAP`. You can then declare subsequent alternate message maps with `ALT_MSG_MAP`. The [END_MSG_MAP](../vs140/END_MSG_MAP.md) macro marks the end of the message map. Every message map must have exactly one instance of `BEGIN_MSG_MAP` and `END_MSG_MAP`.  
  
 For more information about using message maps in ATL, see [Message Maps](../vs140/Message-Maps--ATL-.md).  
  
## Example  
 [!CODE [NVC_ATL_Windowing#108](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#108)]  
  
 This example illustrates the following:  
  
-   If a window procedure is using `CMyClass`'s default message map and `OnPaint` does not handle a message, the message is directed to `m_obj`'s default message map for processing.  
  
-   If a window procedure is using the first alternate message map in `CMyClass`, all messages are directed to `m_obj`'s default message map.  
  
-   If a window procedure is using `CMyClass`'s second alternate message map and `OnChar` does not handle a message, the message is directed to the specified alternate message map of `m_obj`. Class `CMyContainedClass` must have declared this message map with `ALT_MSG_MAP(1)`.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [CHAIN_MSG_MAP](../vs140/CHAIN_MSG_MAP.md)   
 [CHAIN_MSG_MAP_DYNAMIC](../vs140/CHAIN_MSG_MAP_DYNAMIC.md)   
 [MESSAGE_HANDLER](../vs140/MESSAGE_HANDLER.md)