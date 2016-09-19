---
title: "IDiaLoadCallback::NotifyDebugDir"
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
ms.assetid: bd04e2f6-0dbf-4742-a556-96f2cd99aa19
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaLoadCallback::NotifyDebugDir
Called when a debug directory was found in the .exe file.  
  
## Syntax  
  
```cpp#  
HRESULT NotifyDebugDir (   
   BOOL  fExecutable,  
   DWORD cbData,  
   BYTE  data[]  
);  
```  
  
#### Parameters  
 `fExecutable`  
 [in] `TRUE` if the debug directory is read from an executable (rather than a .dbg file).  
  
 `cbData`  
 [in] Count of bytes of data in the debug directory.  
  
 `data[]`  
 [in] An array that is filled in with the debug directory.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. The return code is typically ignored.  
  
## Remarks  
 The [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md) method invokes this callback when it finds a debug directory while processing the executable file.  
  
 This method removes the need for the client to reverse engineer the executable and/or debug file to support debug information other than that found in the .pdb file. With this data, the client can recognize the type of debug information available and whether it resides in the executable file or the .dbg file.  
  
 Most clients will not need this callback because the `IDiaDataSource::loadDataForExe` method transparently opens both .pdb and .dbg files when necessary to serve symbols.  
  
## See Also  
 [IDiaLoadCallback2](../vs140/IDiaLoadCallback2.md)   
 [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md)