---
title: "IDiaSession::findAcceleratorInlineesByLinenum"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 386c87aa-f7b2-4d38-9dd6-fffba9ff01f0
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::findAcceleratorInlineesByLinenum
Returns an enumeration of symbols for inline frames that correspond to the specified source location.  
  
## Syntax  
  
```cpp#  
HRESULT findAcceleratorInlineeLinesByName (   
   IDiaSymbol*           parent,  
   IDiaSourceFile*       file,  
   DWORD                 linenum,  
   DWORD                 colnum,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### Parameters  
 `parent`  
 [in] An `IDiaSymbol` that corresponds to the Accelerator stub function that needs to be searched.  
  
 `file`  
 [in] The `IDiaSourceFile` of the source location.  
  
 `linenum`  
 [in] The line number of the source location.  
  
 `colnum`  
 [in] The column number of the source location.  
  
 `ppResult`  
 [out] A pointer to an `IDiaEnumLineNumbers` interface pointer that is initialized with the result.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaEnumLineNumbers](../vs140/IDiaEnumLineNumbers.md)   
 [IDiaSymbol](../vs140/IDiaSymbol.md)