---
title: "IDiaSession::findFile"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a215dc21-b316-40d7-9923-55bfa014976b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::findFile
Retrieves source files by compiland and name.  
  
## Syntax  
  
```cpp#  
HRESULT findFile (   
   IDiaSymbol*           pCompiland,  
   LPCOLESTR             name,  
   DWORD                 option,  
   IDiaEnumSourceFiles** ppResult  
);  
```  
  
#### Parameters  
 `pCompiland`  
 [in] An [IDiaSymbol](../vs140/IDiaSymbol.md) object representing the compiland to be used as a context for the search. Set this parameter to `NULL` to find source files in all compilands.  
  
 `name`  
 [in] Specifies the name of the source file to be retrieved. Set this parameter to `NULL` for all source files to be retrieved.  
  
 `option`  
 [in] Specifies the comparison options applied to name searching. Values from the [NameSearchOptions Enumeration](../vs140/NameSearchOptions.md) enumeration can be used alone or in combination.  
  
 `ppResult`  
 [out] Returns an [IDiaEnumSourceFiles](../vs140/IDiaEnumSourceFiles.md) object that contains a list of the source files retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Example  
  
```cpp#  
IDiaEnumSourceFiles* pEnum;  
pSession->findFile( NULL, L"sourcefile.cpp", nsFNameExt, &pEnum );  
```  
  
## See Also  
 [IDiaEnumSourceFiles](../vs140/IDiaEnumSourceFiles.md)   
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [NameSearchOptions Enumeration](../vs140/NameSearchOptions.md)