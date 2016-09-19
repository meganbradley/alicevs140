---
title: "IDiaDataSource::loadDataForExe"
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
ms.assetid: d94a1068-f53f-44b5-b6fb-00dec361a7f2
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaDataSource::loadDataForExe
Opens and prepares the debug data associated with the .exe/.dll file.  
  
## Syntax  
  
```cpp#  
HRESULT loadDataForExe (  
   LPCOLESTR executable,  
   LPCOLESTR searchPath,  
   IUnknown* pCallback  
);  
```  
  
#### Parameters  
 executable  
 [in] Path to the .exe or .dll file.  
  
 searchPath  
 [in] Alternate path to search for debug data.  
  
 pCallback  
 [in] An `IUnknown` interface for an object that supports a debug callback interface, such as the [IDiaLoadCallback](../vs140/IDiaLoadCallback.md), [IDiaLoadCallback2](../vs140/IDiaLoadCallback2.md), the [IDiaReadExeAtOffsetCallback](../vs140/IDiaReadExeAtOffsetCallback.md), and/or the [IDiaReadExeAtRVACallback](../vs140/IDiaReadExeAtRVACallback.md) interfaces.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. The following table shows some of the possible error codes for this method.  
  
|Value|Description|  
|-----------|-----------------|  
|E_PDB_NOT_FOUND|Failed to open the file, or the file has an invalid format.|  
|E_PDB_FORMAT|Attempted to access a file with an obsolete format.|  
|E_PDB_INVALID_SIG|Signature does not match.|  
|E_PDB_INVALID_AGE|Age does not match.|  
|E_INVALIDARG|Invalid parameter.|  
|E_UNEXPECTED|Data source has already been prepared.|  
  
## Remarks  
 The debug header of the .exe/.dll file names the associated debug data location.  
  
 This method reads the debug header and then searches for and prepares the debug data. The progress of the search may, optionally, be reported and controlled through callbacks. For example, the [IDiaLoadCallback2::NotifyDebugDir](../vs140/IDiaLoadCallback--NotifyDebugDir.md) is invoked when the `IDiaDataSource::loadDataForExe` method finds and processes a debug directory.  
  
 The [IDiaReadExeAtOffsetCallback](../vs140/IDiaReadExeAtOffsetCallback.md) and [IDiaReadExeAtRVACallback](../vs140/IDiaReadExeAtRVACallback.md) interfaces allow the client application to provide alternative methods for reading data from the executable file when the file cannot be accessed directly through standard file I/O.  
  
 To load a .pdb file without validation, use the [IDiaDataSource::loadDataFromPdb](../vs140/IDiaDataSource--loadDataFromPdb.md) method.  
  
 To validate the .pdb file against specific criteria, use the [IDiaDataSource::loadAndValidateDataFromPdb](../vs140/IDiaDataSource--loadAndValidateDataFromPdb.md) method.  
  
 To load a .pdb file directly from memory, use the [IDiaDataSource::loadDataFromIStream](../vs140/IDiaDataSource--loadDataFromIStream.md) method.  
  
## Example  
  
```cpp#  
class MyCallBack: public IDiaLoadCallback  
{  
...  
};  
MyCallBack callback;  
...  
HRESULT hr = pSource->loadDataForExe( L"myprog.exe", L".\debug", (IUnknown*)&callback);  
if (FAILED(hr))  
{  
    // Report error  
}  
```  
  
## See Also  
 [IDiaDataSource](../vs140/IDiaDataSource.md)   
 [IDiaLoadCallback](../vs140/IDiaLoadCallback.md)   
 [IDiaLoadCallback2](../vs140/IDiaLoadCallback2.md)   
 [IDiaLoadCallback::NotifyDebugDir](../vs140/IDiaLoadCallback--NotifyDebugDir.md)   
 [IDiaReadExeAtOffsetCallback](../vs140/IDiaReadExeAtOffsetCallback.md)   
 [IDiaReadExeAtRVACallback](../vs140/IDiaReadExeAtRVACallback.md)   
 [IDiaDataSource::loadDataFromPdb](../vs140/IDiaDataSource--loadDataFromPdb.md)   
 [IDiaDataSource::loadAndValidateDataFromPdb](../vs140/IDiaDataSource--loadAndValidateDataFromPdb.md)   
 [IDiaDataSource::loadDataFromIStream](../vs140/IDiaDataSource--loadDataFromIStream.md)