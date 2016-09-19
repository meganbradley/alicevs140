---
title: "ON_COMMAND_EX"
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
ms.assetid: 0bb49090-aee8-4203-87c8-dd001d3dd26e
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_COMMAND_EX
This macro maps a command message to an extended command-handler member function.  
  
## Syntax  
  
```  
ON_COMMAND_EX(  
   id,  
   memberFxn  
);  
```  
  
#### Parameters  
 `id`  
 The command ID.  
  
 `memberFxn`  
 The name of the message-handler function to which the command is mapped.  
  
## Remarks  
 An extended form of command message handlers is available for advanced uses. The `ON_COMMAND_EX` macro is used for such message handlers, and it provides a superset of the [ON_COMMAND](../vs140/ON_COMMAND.md) functionality. Extended command-handler member functions take a single parameter, a **UINT** containing the command ID, and return a **BOOL**. The return value should be TRUE to indicate that the command has been handled; otherwise routing will continue to other command target objects.  
  
 For more information, see Technical Note [TN006: Message Maps](../vs140/TN006--Message-Maps.md).  
  
## Requirements  
 Header file: afxmsg_.h  
  
## See Also  
 [ON_COMMAND](../vs140/ON_COMMAND.md)   
 [TN006: Message Maps](../vs140/TN006--Message-Maps.md)