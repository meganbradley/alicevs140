---
title: "ICommandSource::RemoveCommandUIHandler"
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
ms.assetid: dcb490bd-0211-45b1-a0dd-444584e15eb7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandSource::RemoveCommandUIHandler
Removes a user interface command message handler from a command source object.  
  
## Syntax  
  
```  
void RemoveCommandUIHandler(   
   unsigned int cmdID   
);  
```  
  
#### Parameters  
 `cmdID`  
 The command ID.  
  
## Remarks  
 This method removes the user interface command message handler mapped to `cmdID` from the command source object.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)   
 [ICommandSource::AddCommandUIHandler](../vs140/ICommandSource--AddCommandUIHandler.md)