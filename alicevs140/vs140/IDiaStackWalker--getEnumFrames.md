---
title: "IDiaStackWalker::getEnumFrames"
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
ms.assetid: f9f09729-4c34-441c-989c-e0b7339ee32c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaStackWalker::getEnumFrames
Retrieves a stack frame enumerator for x86 platforms.  
  
## Syntax  
  
```cpp#  
HRESULT getEnumFrames(   
   IDiaStackWalkHelper*   pHelper,  
   IDiaEnumStackFrames**  ppEnum  
);  
```  
  
#### Parameters  
 `pHelper`  
 [in] The helper [IDiaStackWalkHelper](../vs140/IDiaStackWalkHelper.md) object.  
  
 `ppEnum`  
 [out] Returns an [IDiaEnumStackFrames](../vs140/IDiaEnumStackFrames.md) object that contains a list of [IDiaStackFrame](../vs140/IDiaStackFrame.md) objects.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 To get a stack frame list on any other platform, call the [IDiaStackWalker::getEnumFrames2](../vs140/IDiaStackWalker--getEnumFrames2.md) method.  
  
## See Also  
 [IDiaStackWalker](../vs140/IDiaStackWalker.md)   
 [IDiaStackWalkHelper](../vs140/IDiaStackWalkHelper.md)   
 [IDiaStackFrame](../vs140/IDiaStackFrame.md)   
 [IDiaStackWalker::getEnumFrames2](../vs140/IDiaStackWalker--getEnumFrames2.md)