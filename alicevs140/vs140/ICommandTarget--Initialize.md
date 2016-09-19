---
title: "ICommandTarget::Initialize"
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
ms.assetid: f580a1f4-d711-4b22-8651-6c1314536a11
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandTarget::Initialize
Initializes the command target object.  
  
## Syntax  
  
```  
void Initialize(  
   ICommandSource^ cmdSource  
);  
```  
  
#### Parameters  
 `cmdSource`  
 A handle to the command source object.  
  
## Remarks  
 When you host a user control in an MFC View, [CWinFormsView](../Topic/CWinFormsView%20Class.md) routes commands and update command UI messages to the user control to allow it to handle MFC commands.  
  
 This method initializes the command target object and associates it with the specified command source object `cmdSource`. It should be called in the user control class implementation. At initialization, you should register command handlers with the command source object by calling [ICommandSource::AddCommandHandler](../vs140/ICommandSource--AddCommandHandler.md) in the `Initialize` implementation. See [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md) for an example of how to use `Initialize` to do this.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [ICommandTarget Interface](../vs140/ICommandTarget-Interface.md)   
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)