---
title: "IDiaSession::findAcceleratorInlineesByName"
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
ms.assetid: e203e5c2-6563-43fa-be56-3063955043ab
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::findAcceleratorInlineesByName
Returns an enumeration of symbols for inline frames corresponding to the specified inline function name.  
  
## Syntax  
  
```cpp#  
HRESULT findAcceleratorInlineeLinesByName (   
   LPCOLESTR             name,  
   DWORD                 option,  
   IDiaEnumSymbols**     ppResult  
);  
```  
  
#### Parameters  
 `name`  
 [in] The inlinee function name to be searched.  
  
 `option`  
 [in] The name search options to be used when searching for inline frames that correspond to `name`. For more information, see [NameSearchOptions](../vs140/NameSearchOptions.md).  
  
 `ppResult`  
 [out] A pointer to an `IDiaEnumSymbols` interface pointer that is initialized with the result.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This function searches for inlinees only within Accelerator stub functions. It ignores native C++ procedure records.  
  
## See Also  
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaEnumSymbols](../vs140/IDiaEnumSymbols.md)   
 [IDiaSymbol](../vs140/IDiaSymbol.md)