---
title: "IDebugProcess3::GetHostingProcessLanguage"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 52fca002-a9ef-43b1-9192-afbe7bb59ad4
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess3::GetHostingProcessLanguage
This method returns a `GUID` representing the language of this process as set by a call to [IDebugProcess3::SetHostingProcessLanguage](../vs140/IDebugProcess3--SetHostingProcessLanguage.md).  
  
## Syntax  
  
```cpp  
HRESULT GetHostingProcessLanguage(  
   GUID* pguidLang  
);  
```  
  
```c#  
int GetHostingProcessLanguage(  
   out Guid pguidLang  
);  
```  
  
#### Parameters  
 `pguidLang`  
 [out] The `GUID` of the language of this process. `GUID_NULL` (C++) or `Guid.Empty` (C#) means that the language is not set.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## See Also  
 [IDebugProcess3](../vs140/IDebugProcess3.md)   
 [IDebugProcess3::SetHostingProcessLanguage](../vs140/IDebugProcess3--SetHostingProcessLanguage.md)