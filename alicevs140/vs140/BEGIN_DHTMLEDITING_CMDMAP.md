---
title: "BEGIN_DHTMLEDITING_CMDMAP"
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
ms.assetid: 807e6e85-fb31-4197-9190-be5efbeb4953
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_DHTMLEDITING_CMDMAP
Starts the definition of a DHTML editing command map within a class.  
  
## Syntax  
  
```  
  
BEGIN_DHTMLEDITING_CMDMAP(  
className  
)  
  
```  
  
#### Parameters  
 `className`  
 The name of the class containing the DHTML editing command map. This class should derive directly or indirectly from [CHtmlEditView](../vs140/CHtmlEditView-Class.md) and include the [DECLARE_DHTMLEDITING_CMDMAP](../vs140/DECLARE_DHTMLEDITING_CMDMAP.md) macro within its class definition.  
  
## Remarks  
 Add a DHTML editing command map to your class to map user interface commands to HTML editing commands.  
  
 Place the `BEGIN_DHTMLEDITING_CMDMAP` macro in the class's implementation (.cpp) file followed by [DHTMLEDITING_CMD_ENTRY](../vs140/DHTMLEDITING_CMD_ENTRY.md) macros for the commands the class is to map (for example, from **ID_EDIT_CUT** to **IDM_CUT**). Use the [END_DHTMLEDITING_CMDMAP](../vs140/END_DHTMLEDITING_CMDMAP.md) macro to mark the end of the event map.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DHTML Editing Command Maps](../vs140/DHTML-Editing-Command-Maps.md)