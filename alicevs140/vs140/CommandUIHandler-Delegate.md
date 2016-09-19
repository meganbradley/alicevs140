---
title: "CommandUIHandler Delegate"
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
ms.assetid: 2da11ecc-20d6-4a53-97fc-08b48f06d71a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CommandUIHandler Delegate
Registers callback methods with a user interface update command message.  
  
## Syntax  
  
```  
delegate void CommandUIHandler(  
   unsigned int cmdID,  
   ICommandUI^ cmdUI  
);  
```  
  
#### Parameters  
 `cmdID`  
 The command ID.  
  
 `cmdUI`  
 The command message ID.  
  
## Remarks  
 This delegate registers callback methods with a user interface update command message. `CommandUIHandler` is similar to [CommandHandler](../vs140/CommandHandler-Delegate.md) except that this delegate is used with user interface object update commands. User interface update commands should be mapped one-to-one with message handler methods.  
  
 For more information on using Windows Forms, see [Using Windows Forms in MFC](../vs140/Using-a-Windows-Form-User-Control-in-MFC.md).  
  
## Requirements  
 **Header:** afxwinforms.h (defined in assembly atlmfc\lib\mfcmifc80.dll)  
  
## See Also  
 [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md)   
 [CommandHandler Delegate](../vs140/CommandHandler-Delegate.md)