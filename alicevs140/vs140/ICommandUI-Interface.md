---
title: "ICommandUI Interface"
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
ms.assetid: 134afe8d-dcdf-47ca-857a-a166a6b665dd
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandUI Interface
Manages user interface commands.  
  
## Syntax  
  
```  
interface class ICommandUI  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ICommandUI::Check](../vs140/ICommandUI--Check.md)|Sets the user interface item for this command to the appropriate check state.|  
|[ICommandUI::ContinueRouting](../vs140/ICommandUI--ContinueRouting.md)|Tells the command-routing mechanism to continue routing the current message down the chain of handlers.|  
|[ICommandUI::Enabled](../vs140/ICommandUI--Enabled.md)|Enables or disables the user interface item for this command.|  
|[ICommandUI::ID](../vs140/ICommandUI--ID.md)|Gets the ID of the user interface object represented by the `ICommandUI` object.|  
|[ICommandUI::Index](../vs140/ICommandUI--Index.md)|Gets the index of the user interface object represented by the `ICommandUI` object.|  
|[ICommandUI::Radio](../vs140/ICommandUI--Radio.md)|Sets the user interface item for this command to the appropriate check state.|  
|[ICommandUI::Text](../vs140/ICommandUI--Text.md)|Sets the text of the user interface item for this command.|  
  
## Remarks  
 This interface provides methods and properties that manage user interface commands. `ICommandUI` is similar to [CCmdUI](../vs140/CCmdUI-Class.md), except that `ICommandUI` is used for MFC applications that interoperate with .NET components.  
  
 `ICommandUI` is used within an `ON_UPDATE_COMMAND_UI` handler in an [ICommandTarget](../vs140/ICommandTarget-Interface.md)-derived class. When a user of an application activates (selects or clicks) a menu, each menu item is displayed as enabled or disabled. The target of each menu command provides this information by implementing an `ON_UPDATE_COMMAND_UI` handler. For each of the command user interface objects in your application, use the Properties window to create a message-map entry and function prototype for each handler.  
  
 For more information on how the `ICommandUI` interface is used in command routing, see [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md).  
  
 For more information on using Windows Forms, see [Using Windows Forms in MFC](../vs140/Using-a-Windows-Form-User-Control-in-MFC.md).  
  
 For more information on how user interface commands are managed in MFC, see [CCmdUI](../vs140/CCmdUI-Class.md).  
  
## Requirements  
 **Header:** afxwinforms.h (defined in assembly atlmfc\lib\mfcmifc80.dll)  
  
## See Also  
 [CCmdUI Class](../vs140/CCmdUI-Class.md)