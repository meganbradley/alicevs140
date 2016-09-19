---
title: "IDebugProgramPublisher2::PublishProgram"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 92ff63f0-e869-4040-b3ae-b2c899e708ff
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramPublisher2::PublishProgram
This method makes a program available for debug engines (DEs) and the session debug manager.  
  
## Syntax  
  
```cpp  
HRESULT PublishProgram(  
   CONST_GUID_ARRAY Engines,  
   LPCOLESTR        szFriendlyName,  
   IUnknown*        pDebuggeeInterface  
);  
```  
  
```c#  
int PublishProgram(  
   CONST_GUID_ARRAY Engines,  
   string           szFriendlyName,  
   object           pDebuggeeInterface  
);  
```  
  
#### Parameters  
 `Engines`  
 [in] An array of GUIDs for DEs that can launch or attach to this program.  
  
 `szFriendlyName`  
 [in] Friendly name for the program (this appears in menus or dialogs presented to the user).  
  
 `pDebuggeeInterface`  
 [in] `IUnknown` interface for the program (this value is used as a cookie to uniquely identify the program; this same value is used to "unpublish" the program)  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 To make a program no longer available for debugging, call [IDebugProgramPublisher2::UnpublishProgram](../vs140/IDebugProgramPublisher2--UnpublishProgram.md).  
  
## See Also  
 [IDebugProgramPublisher2](../vs140/IDebugProgramPublisher2.md)   
 [IDebugProgramPublisher2::UnpublishProgram](../vs140/IDebugProgramPublisher2--UnpublishProgram.md)