---
title: "IDiaEnumStackFrames::Next"
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
ms.assetid: 09378a21-d5e3-4213-b7e2-10f04d85295f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumStackFrames::Next
Retrieves a specified number of stack frame elements from the enumeration sequence.  
  
## Syntax  
  
```cpp#  
HRESULT Next(   
   ULONG             celt,  
   IDiaStackFrame**  rgelt,  
   ULONG*            pceltFetched  
);  
```  
  
#### Parameters  
 celt  
 [in] The number of stackframe elements in the enumerator to be retrieved.  
  
 rgelt  
 [out] An array that is to be filled in with the requested [IDiaStackFrame](../vs140/IDiaStackFrame.md) objects.  
  
 pceltFetched  
 [out] Returns the number of stack frame elements in the fetched enumerator.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if there are no more stack frames. Otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumStackFrames](../vs140/IDiaEnumStackFrames.md)   
 [IDiaStackFrame](../vs140/IDiaStackFrame.md)