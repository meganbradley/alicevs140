---
title: "ICommandSource Interface"
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
ms.assetid: a4b1f698-c09f-4ba8-9b13-0e74a0a4967e
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandSource Interface
Manages commands sent from a command source object to a user control.  
  
## Syntax  
  
```  
interface class ICommandSource  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ICommandSource::AddCommandHandler](../vs140/ICommandSource--AddCommandHandler.md)|Adds a command handler to a command source object.|  
|[ICommandSource::AddCommandRangeHandler](../vs140/ICommandSource--AddCommandRangeHandler.md)|Adds a group of command handlers to a command source object.|  
|[ICommandSource::AddCommandRangeUIHandler](../vs140/ICommandSource--AddCommandRangeUIHandler.md)|Adds a group of user interface command message handlers to a command source object.|  
|[ICommandSource::AddCommandUIHandler](../vs140/ICommandSource--AddCommandUIHandler.md)|Adds a user interface command message handler to a command source object.|  
|[ICommandSource::PostCommand](../vs140/ICommandSource--PostCommand.md)|Posts a message without waiting for it to be processed.|  
|[ICommandSource::RemoveCommandHandler](../vs140/ICommandSource--RemoveCommandHandler.md)|Removes a command handler from a command source object.|  
|[ICommandSource::RemoveCommandRangeHandler](../vs140/ICommandSource--RemoveCommandRangeHandler.md)|Removes a group of command handlers from a command source object.|  
|[ICommandSource::RemoveCommandRangeUIHandler](../vs140/ICommandSource--RemoveCommandRangeUIHandler.md)|Removes a group of user interface command message handlers from a command source object.|  
|[ICommandSource::RemoveCommandUIHandler](../vs140/ICommandSource--RemoveCommandUIHandler.md)|Removes a user interface command message handler from a command source object.|  
|[ICommandSource::SendCommand](../vs140/ICommandSource--SendCommand.md)|Sends a message and waits for it to be processed before returning.|  
  
## Remarks  
 When you host a user control in an MFC View, [CWinFormsView](../Topic/CWinFormsView%20Class.md) routes commands and update command UI messages to the user control to allow it to handle MFC commands (for example, frame menu items and toolbar buttons). By implementing [ICommandTarget](../vs140/ICommandTarget-Interface.md), you give the user control a reference to the `ICommandSource` object.  
  
 See [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md) for an example of how to use `ICommandTarget`.  
  
 For more information on using Windows Forms, see [Using Windows Forms in MFC](../vs140/Using-a-Windows-Form-User-Control-in-MFC.md).  
  
## Requirements  
 **Header:** afxwinforms.h (defined in assembly atlmfc\lib\mfcmifc80.dll)  
  
## See Also  
 [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md)   
 [ICommandTarget Interface](../vs140/ICommandTarget-Interface.md)