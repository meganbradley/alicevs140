---
title: "IDebugCodeContext2::GetLanguageInfo"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 03002ef1-9fe6-44b6-b23b-ef7b86b2b21b
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCodeContext2::GetLanguageInfo
Gets the language information for this code context.  
  
## Syntax  
  
```cpp#  
HRESULT GetLanguageInfo(   
   BSTR* pbstrLanguage,  
   GUID* pguidLanguage  
);  
```  
  
```c#  
int GetLanguageInfo(   
   ref string pbstrLanguage,  
   ref Guid pguidLanguage  
);  
```  
  
#### Parameters  
 `pbstrLanguage`  
 [in, out] Returns a string that contains the name of the language, such as "C++."  
  
 `pguidLanguage`  
 [in, out] Returns the GUID for the language of the code context, for example, `guidCPPLang`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 At least one of the parameters must return a non-null value.  
  
## See Also  
 [IDebugCodeContext2](../vs140/IDebugCodeContext2.md)