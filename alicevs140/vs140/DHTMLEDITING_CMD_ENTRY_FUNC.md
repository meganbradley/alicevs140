---
title: "DHTMLEDITING_CMD_ENTRY_FUNC"
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
ms.topic: article
ms.assetid: a9c086f7-3615-4f2c-ad4b-969efd6b6580
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DHTMLEDITING_CMD_ENTRY_FUNC
Maps a command ID to an HTML editing command and message handler.  
  
## Syntax  
  
```  
  
DHTMLEDITING_CMD_ENTRY_FUNC(  
cmdID  
,   
dhtmlcmdID  
,   
member_func_name  
)  
  
```  
  
#### Parameters  
 `cmdID`  
 The command ID (such as **ID_EDIT_COPY**).  
  
 `dhtmlcmdID`  
 The HTML editing command to which `cmdID` maps (such as **IDM_COPY**).  
  
 `member_func_name`  
 The name of the message-handler function to which the command is mapped.  
  
## Example  
 See [HTMLEdit Sample](../vs140/Visual-C---Samples.md).  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DHTML Editing Command Maps](../vs140/DHTML-Editing-Command-Maps.md)   
 [DHTMLEDITING_CMD_ENTRY](../vs140/DHTMLEDITING_CMD_ENTRY.md)   
 [DHTMLEDITING_CMD_ENTRY_FUNC_TYPE](../vs140/DHTMLEDITING_CMD_ENTRY_FUNC_TYPE.md)   
 [DHTMLEDITING_CMD_ENTRY_TYPE](../vs140/DHTMLEDITING_CMD_ENTRY_TYPE.md)