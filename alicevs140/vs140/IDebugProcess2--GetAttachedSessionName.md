---
title: "IDebugProcess2::GetAttachedSessionName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e5e116f-2c0c-4bc8-ad3f-e9fd2318a7e4
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess2::GetAttachedSessionName
Gets the name of the session that is debugging this process. An IDE can display this information to a user who is debugging a particular process on a particular machine.  
  
> [!NOTE]
>  This method is deprecated, and its implementation should always return `E_NOTIMPL`.  
  
## Syntax  
  
```  
HRESULT GetAttachedSessionName(  
   BSTR* pbstrSessionName  
);  
```  
  
#### Parameters  
 `pbstrSessionName`  
  
## Return Value  
 This method should always return `E_NOTIMPL`.  
  
## See Also  
 [IDebugProcess2](../vs140/IDebugProcess2.md)