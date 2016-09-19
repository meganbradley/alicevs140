---
title: "ICommandSource::AddCommandHandler"
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
ms.assetid: 0829f789-bf15-4c62-ab41-9ae32925d78d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandSource::AddCommandHandler
Adds a command handler to a command source object.  
  
## Syntax  
  
```  
void AddCommandHandler(  
   unsigned int cmdID,  
   CommandHandler^ cmdHandler  
);  
```  
  
#### Parameters  
 `cmdID`  
 The command ID.  
  
 `cmdHandler`  
 A handle to the command handler method.  
  
## Remarks  
 This method adds the command handler `cmdHandler` to the command source object and maps the handler to `cmdID`.  
  
 See [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md) for an example of how to use `AddCommandHandler`.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)   
 [ICommandSource::RemoveCommandHandler](../vs140/ICommandSource--RemoveCommandHandler.md)