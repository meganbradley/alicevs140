---
title: "CommandHandler Delegate"
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
ms.assetid: 22096734-e074-4aca-8523-4b15590109f9
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CommandHandler Delegate
Registers callback methods with a command source.  
  
## Syntax  
  
```  
delegate void CommandHandler(  
   UINT^ cmdID  
);  
```  
  
#### Parameters  
 `cmdID`  
 The command ID.  
  
## Remarks  
 This delegate registers callback methods with a command source. When you add a delegate to the command source object, the callback method becomes a handler for commands coming from the specified source.  
  
 For more information, see [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md).  
  
 For more information on using Windows Forms, see [Using Windows Forms in MFC](../vs140/Using-a-Windows-Form-User-Control-in-MFC.md).  
  
## Requirements  
 **Header:** afxwinforms.h (defined in assembly atlmfc\lib\mfcmifc80.dll)  
  
## See Also  
 [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md)