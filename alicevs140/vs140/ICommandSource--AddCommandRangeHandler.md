---
title: "ICommandSource::AddCommandRangeHandler"
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
ms.assetid: f86cc4ea-acac-4523-8225-20a7fb182cec
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandSource::AddCommandRangeHandler
Adds a group of command handlers to a command source object.  
  
## Syntax  
  
```  
void AddCommandRangeHandler(  
   unsigned int cmdIDMin,  
   unsigned int cmdIDMax,  
   CommandHandler^ cmdHandler  
);  
```  
  
#### Parameters  
 `cmdIDMin`  
 The beginning index of the command ID range.  
  
 `cmdIDMax`  
 The ending index of the command ID range.  
  
 `cmdHandler`  
 A handle to the message handler method to which the commands are mapped.  
  
## Remarks  
 This method maps a contiguous range of command IDs to a single message handler and adds it to the command source object. This is used for handling a group of related buttons with one method.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)   
 [ICommandSource::RemoveCommandRangeHandler](../vs140/ICommandSource--RemoveCommandRangeHandler.md)