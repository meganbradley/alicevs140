---
title: "ALT_MSG_MAP"
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
ms.assetid: 2c8871bf-abc0-4d52-bcf7-6b2ab9eb5af8
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ALT_MSG_MAP
Marks the beginning of an alternate message map.  
  
## Syntax  
  
```  
  
ALT_MSG_MAP( msgMapID )  
```  
  
#### Parameters  
 `msgMapID`  
 [in] The message map identifier.  
  
## Remarks  
 ATL identifies each message map by a number. The default message map (declared with the `BEGIN_MSG_MAP` macro) is identified by 0. An alternate message map is identified by `msgMapID`.  
  
 Message maps are used to process messages sent to a window. For example, [CContainedWindow](../vs140/CContainedWindowT-Class.md) allows you to specify the identifier of a message map in the containing object. [CContainedWindow::WindowProc](../vs140/CContainedWindowT--WindowProc.md) then uses this message map to direct the contained window's messages either to the appropriate handler function or to another message map. For a list of macros that declare handler functions, see [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md).  
  
 Always begin a message map with `BEGIN_MSG_MAP`. You can then declare subsequent alternate message maps.  
  
 The [END_MSG_MAP](../vs140/END_MSG_MAP.md) macro marks the end of the message map. Note that there is always exactly one instance of `BEGIN_MSG_MAP` and `END_MSG_MAP`.  
  
 For more information about using message maps in ATL, see [Message Maps](../vs140/Message-Maps--ATL-.md).  
  
## Example  
 The following example shows the default message map and one alternate message map, each containing one handler function:  
  
 [!CODE [NVC_ATL_Windowing#98](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#98)]  
  
 The next example shows two alternate message maps. The default message map is empty.  
  
 [!CODE [NVC_ATL_Windowing#99](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#99)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [MESSAGE_HANDLER](../vs140/MESSAGE_HANDLER.md)   
 [CMessageMap Class](../vs140/CMessageMap-Class.md)   
 [CDynamicChain Class](../vs140/CDynamicChain-Class.md)