---
title: "IDebugSymbolProvider::GetLanguage"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e4142183-3d8b-418f-907f-4ee4c753d8ce
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugSymbolProvider::GetLanguage
This method gets the language that was used to compile the code at the debug address.  
  
## Syntax  
  
```cpp#  
HRESULT GetLanguage(   
   IDebugAddress* pAddress,  
   GUID*          pguidLanguage,  
   GUID*          pguidLanguageVendor  
);  
```  
  
```c#  
int GetLanguage(  
   IDebugAddress pAddress,   
   out Guid      pguidLanguage,   
   out Guid      pguidLanguageVendor  
);  
```  
  
#### Parameters  
 `pAddress`  
 [in] An address object represented by an [IDebugAddress](../vs140/IDebugAddress.md) interface.  
  
 `pguidLanguage`  
 [out] Returns a `GUID` that specifies the language.  
  
 `pguidLanguageVendor`  
 [out] Returns a `GUID` that specifies the language vendor.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The debug engine calls this method to obtain the information it needs to select the correct expression evaluator.  
  
## See Also  
 [IDebugSymbolProvider](../vs140/IDebugSymbolProvider.md)   
 [IDebugAddress](../vs140/IDebugAddress.md)