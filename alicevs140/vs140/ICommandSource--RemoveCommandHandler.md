---
title: "ICommandSource::RemoveCommandHandler"
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
ms.assetid: 2d0c6aba-57cf-4b75-b5a7-3902ab0fbcbd
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandSource::RemoveCommandHandler
Removes a command handler from a command source object.  
  
## Syntax  
  
```  
void RemoveCommandHandler(  
   unsigned int cmdID  
);  
```  
  
#### Parameters  
 `cmdID`  
 The command ID.  
  
## Remarks  
 This method removes the command handler mapped to `cmdID` from the command source object.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)   
 [ICommandSource::AddCommandHandler](../vs140/ICommandSource--AddCommandHandler.md)