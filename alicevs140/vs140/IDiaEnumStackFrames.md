---
title: "IDiaEnumStackFrames"
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
ms.assetid: 3d1e8403-c9fc-42ff-ae35-0ab9a5ed2ad7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumStackFrames
Enumerates the various stack frames available.  
  
## Methods in Vtable Order  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaEnumStackFrames::Next](../vs140/IDiaEnumStackFrames--Next.md)|Retrieves a specified number of stack frame elements from the enumeration sequence.|  
|[IDiaEnumStackFrames::Reset](../vs140/IDiaEnumStackFrames--Reset.md)|Resets an enumeration sequence to the beginning.|  
  
## Remarks  
  
## Notes for Callers  
 Obtain this interface by calling the [IDiaStackWalker::getEnumFrames](../vs140/IDiaStackWalker--getEnumFrames.md) or [IDiaStackWalker::getEnumFrames2](../vs140/IDiaStackWalker--getEnumFrames2.md) methods.  
  
## Example  
 This example shows how to obtain and use the `IDiaEnumStackFrames` interface. See the [IDiaStackFrame](../vs140/IDiaStackFrame.md) interface for an implementation of the `PrintStackFrame` function.  
  
```cpp#  
void DumpStackFrames(IDiaStackWalker*     pStackWalker,  
                     IDiaStackWalkHelper* pStackWalkHelper,  
                     CV_CPU_TYPE_e        cpuType)  
{  
    if (pStackWalker != NULL && pStackWalkHelper != NULL)  
    {  
        CComPtr<IDiaEnumStackFrames> pEnumsFrames;  
        HRESULT hr;  
        hr = pStackWalker->getEnumFrames2(cpuType, pStackWalkHelper, &pEnumFrames);  
        if (SUCCEEDED(hr) && pEnumFrames != NULL)  
        {  
             CComPtr<IDiaStackFrame> pStackFrame;  
             DWORD celt = 0;  
  
             while (pEnumFrames->Next(1, &pStackFrame, &celt) == S_OK)  
             {  
                 PrintStackFrame(pStackFrame);  
             }  
             pStackFrame = NULL;  
        }  
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaStackWalkFrame](../vs140/IDiaStackWalkFrame.md)   
 [IDiaStackWalker::getEnumFrames2](../vs140/IDiaStackWalker--getEnumFrames2.md)   
 [IDiaStackWalker::getEnumFrames](../vs140/IDiaStackWalker--getEnumFrames.md)