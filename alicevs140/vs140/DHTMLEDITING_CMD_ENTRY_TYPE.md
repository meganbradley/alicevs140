---
title: "DHTMLEDITING_CMD_ENTRY_TYPE"
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
ms.assetid: 140fa0e8-3019-472f-9acf-8015ca76d7ce
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DHTMLEDITING_CMD_ENTRY_TYPE
Maps a command ID to an HTML editing command and user interface element.  
  
## Syntax  
  
```  
  
DHTMLEDITING_CMD_ENTRY_TYPE(  
cmdID  
,   
dhtmlcmdID  
,   
elemType  
)  
  
```  
  
#### Parameters  
 `cmdID`  
 The command ID (such as **ID_EDIT_COPY**).  
  
 `dhtmlcmdID`  
 The HTML editing command to which `cmdID` maps (such as **IDM_COPY**).  
  
 `elemType`  
 The user interface element type; one of **AFX_UI_ELEMTYPE_NORMAL**, **AFX_UI_ELEMTYPE_CHECKBOX**, or **AFX_UI_ELEMTYPE_RADIO**.  
  
## Example  
 See [HTMLEdit Sample](../vs140/Visual-C---Samples.md).  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DHTML Editing Command Maps](../vs140/DHTML-Editing-Command-Maps.md)   
 [DHTMLEDITING_CMD_ENTRY](../vs140/DHTMLEDITING_CMD_ENTRY.md)   
 [DHTMLEDITING_CMD_ENTRY_FUNC](../vs140/DHTMLEDITING_CMD_ENTRY_FUNC.md)   
 [DHTMLEDITING_CMD_ENTRY_FUNC_TYPE](../vs140/DHTMLEDITING_CMD_ENTRY_FUNC_TYPE.md)