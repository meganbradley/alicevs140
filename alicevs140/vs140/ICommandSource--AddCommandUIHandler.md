---
title: "ICommandSource::AddCommandUIHandler"
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
ms.assetid: f0c9523b-fc75-4721-bc7b-8c6e7e00539a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandSource::AddCommandUIHandler
Adds a user interface command message handler to a command source object.  
  
## Syntax  
  
```  
void AddCommandUIHandler(   
   unsigned int cmdID,   
   CommandUIHandler^ cmdUIHandler   
);  
```  
  
#### Parameters  
 `cmdID`  
 The command ID.  
  
 `cmdUIHandler`  
 A handle to the user interface command message handler method.  
  
## Remarks  
 This method adds the user interface command message handler `cmdHandler` to the command source object and maps the handler to `cmdID`.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)   
 [ICommandSource::RemoveCommandUIHandler](../vs140/ICommandSource--RemoveCommandUIHandler.md)