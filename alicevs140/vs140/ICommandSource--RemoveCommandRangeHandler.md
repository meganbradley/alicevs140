---
title: "ICommandSource::RemoveCommandRangeHandler"
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
ms.assetid: 7e74a854-6918-465d-98fe-3ea29a2a79b6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandSource::RemoveCommandRangeHandler
Removes a group of command handlers from a command source object.  
  
## Syntax  
  
```  
void RemoveCommandRangeUIHandler(  
   unsigned int cmdIDMin,  
   unsigned int cmdIDMax  
);  
```  
  
#### Parameters  
 `cmdIDMin`  
 The beginning index of the command ID range.  
  
 `cmdIDMax`  
 The ending index of the command ID range.  
  
## Remarks  
 This method removes a group of message handlers, mapped to the command IDs specifed by `cmdIDMin` and `cmdIDMax`, from the command source object.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)   
 [ICommandSource::AddCommandRangeHandler](../vs140/ICommandSource--AddCommandRangeHandler.md)