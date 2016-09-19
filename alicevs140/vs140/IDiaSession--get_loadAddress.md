---
title: "IDiaSession::get_loadAddress"
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
ms.assetid: 5162ae1a-38e3-4571-8995-4ed9be1dec3e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::get_loadAddress
Retrieves the load address for the executable file that corresponds to the symbols in this symbol store.  
  
## Syntax  
  
```cpp#  
HRESULT get_loadAddress (   
   ULONGLONG* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns a virtual address (VA) where an .exe file or .dll file is loaded.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The returned load address is always zero unless specifically set using the [IDiaSession::put_loadAddress](../vs140/IDiaSession--put_loadAddress.md) method.  
  
## See Also  
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaSession::put_loadAddress](../vs140/IDiaSession--put_loadAddress.md)