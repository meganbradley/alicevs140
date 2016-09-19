---
title: "IDiaEnumSourceFiles::Next"
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
ms.assetid: 83bf6317-ff39-4c5c-8987-cba34e7a6983
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumSourceFiles::Next
Retrieves a specified number of source files in the enumeration sequence.  
  
## Syntax  
  
```cpp#  
HRESULT Next (   
   ULONG            celt,  
   IDiaSourceFile** rgelt,  
   ULONG*           pceltFetched  
);  
```  
  
#### Parameters  
 celt  
 [in] The number of source files in the enumerator to be retrieved.  
  
 rgelt  
 [out]An array that is to be filled in with the [IDiaSourceFile](../vs140/IDiaSourceFile.md) objects that represent the desired source files.  
  
 pceltFetched  
 [out] Returns the number of source files in the fetched enumerator.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if there are no more source files. Otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumSourceFiles](../vs140/IDiaEnumSourceFiles.md)   
 [IDiaSession::findLinesByLinenum](../vs140/IDiaSession--findLinesByLinenum.md)   
 [IDiaSourceFile](../vs140/IDiaSourceFile.md)