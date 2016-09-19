---
title: "ICommandTarget Interface"
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
ms.assetid: dd9927f6-3479-4e7c-8ef9-13206cf901f3
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ICommandTarget Interface
Provides a user control with an interface to receive commands from a command source object.  
  
## Syntax  
  
```  
interface class ICommandTarget  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ICommandTarget::Initialize](../vs140/ICommandTarget--Initialize.md)|Initializes the command target object.|  
  
## Remarks  
 When you host a user control in an MFC View, [CWinFormsView](../Topic/CWinFormsView%20Class.md) routes commands and update command UI messages to the user control to allow it to handle MFC commands (for example, frame menu items and toolbar buttons). By implementing `ICommandTarget`, you give the user control a reference to the [ICommandSource](../vs140/ICommandSource-Interface.md) object.  
  
 See [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md) for an example of how to use `ICommandTarget`.  
  
 For more information on using Windows Forms, see [Using Windows Forms in MFC](../vs140/Using-a-Windows-Form-User-Control-in-MFC.md).  
  
## Requirements  
 **Header:** afxwinforms.h (defined in assembly atlmfc\lib\mfcmifc80.dll)  
  
## See Also  
 [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md)   
 [ICommandSource Interface](../vs140/ICommandSource-Interface.md)