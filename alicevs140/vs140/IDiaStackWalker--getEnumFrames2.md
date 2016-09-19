---
title: "IDiaStackWalker::getEnumFrames2"
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
ms.assetid: 73196d3f-112c-4b3a-997b-7c6b815d4afc
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaStackWalker::getEnumFrames2
Retrieves a stack frame enumerator for a specific platform type.  
  
## Syntax  
  
```cpp#  
  
      HRESULT getEnumFrames2(   
   enum  CV_CPU_TYPE_e    cpuid,  
   IDiaStackWalkHelper*   pHelper,  
   IDiaEnumStackFrames**  ppEnum  
);  
```  
  
#### Parameters  
 `cpuid`  
 [in] A value from the [CV_CPU_TYPE_e Enumeration](../vs140/CV_CPU_TYPE_e.md) enumeration, specifying the platform type.  
  
 `pHelper`  
 [in] The helper [IDiaStackWalkHelper](../vs140/IDiaStackWalkHelper.md) object.  
  
 `ppEnum`  
 [out] Returns an [IDiaEnumStackFrames](../vs140/IDiaEnumStackFrames.md) object containing a list of [IDiaStackFrame](../vs140/IDiaStackFrame.md) objects.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 To obtain a stack frame list for just the x86 platform, call the [IDiaStackWalker::getEnumFrames](../vs140/IDiaStackWalker--getEnumFrames.md) method.  
  
## See Also  
 [IDiaStackWalker](../vs140/IDiaStackWalker.md)   
 [CV_CPU_TYPE_e Enumeration](../vs140/CV_CPU_TYPE_e.md)   
 [IDiaStackWalkHelper](../vs140/IDiaStackWalkHelper.md)   
 [IDiaStackFrame](../vs140/IDiaStackFrame.md)   
 [IDiaStackWalker::getEnumFrames](../vs140/IDiaStackWalker--getEnumFrames.md)