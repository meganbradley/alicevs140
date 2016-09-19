---
title: "IDebugProcess3::SetHostingProcessLanguage"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e42f33ed-f29c-4e45-92ce-ab504b72d77c
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess3::SetHostingProcessLanguage
This method sets the language that the process will be hosted under. This language can then be used by the debug engine (DE) to load the appropriate expression evaluator.  
  
## Syntax  
  
```cpp  
HRESULT SetHostingProcessLanguage(  
   REFGUID guidLang  
);  
```  
  
```c#  
int SetHostingProcessLanguage(  
   ref Guid guidLang  
);  
```  
  
#### Parameters  
 `guidLang`  
 [in] `GUID` of the language that the DE should use. Specify `GUID_NULL` (C++) or `Guid.Empty` (C#) to have the DE use the default language.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## Remarks  
 [IDebugProcess3::GetHostingProcessLanguage](../vs140/IDebugProcess3--GetHostingProcessLanguage.md) can be used to retrieve the current language setting.  
  
## See Also  
 [IDebugProcess3](../vs140/IDebugProcess3.md)   
 [IDebugProcess3::GetHostingProcessLanguage](../vs140/IDebugProcess3--GetHostingProcessLanguage.md)