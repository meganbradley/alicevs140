---
title: "IDiaDataSource"
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
ms.assetid: 6260ac76-4f9d-4144-ba22-32f8620b32c2
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaDataSource
Initiates access to a source of debugging symbols.  
  
## Syntax  
  
```  
IDiaDataSource : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaDataSource`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaDataSource::get_lastError](../vs140/IDiaDataSource--get_lastError.md)|Retrieves the file name for the last load error.|  
|[IDiaDataSource::loadDataFromPdb](../vs140/IDiaDataSource--loadDataFromPdb.md)|Opens and prepares a program database (.pdb) file as a debug data source.|  
|[IDiaDataSource::loadAndValidateDataFromPdb](../vs140/IDiaDataSource--loadAndValidateDataFromPdb.md)|Opens and verifies that the program database (.pdb) file matches the signature information provided; prepares the .pdb file as a debug data source.|  
|[IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md)|Opens and prepares the debug data associated with the .exe/.dll file.|  
|[IDiaDataSource::loadDataFromIStream](../vs140/IDiaDataSource--loadDataFromIStream.md)|Prepares the debug data stored in a program database (.pdb) file accessed through an in-memory data stream.|  
|[IDiaDataSource::openSession](../vs140/IDiaDataSource--openSession.md)|Opens a session for querying symbols.|  
  
## Remarks  
 A call to one of the load methods of the `IDiaDataSource` interface opens the symbol source. A successful call to the [IDiaDataSource::openSession](../vs140/IDiaDataSource--openSession.md) method returns an [IDiaSession](../vs140/IDiaSession.md) interface that supports querying the data source. If the load method returns a file-related error then the [IDiaDataSource::get_lastError](../vs140/IDiaDataSource--get_lastError.md) method return value contains the file name associated with the error.  
  
## Notes for Callers  
 This interface is obtained by calling the `CoCreateInstance` function with the class identifier `CLSID_DiaSource` and the interface ID of `IID_IDiaDataSource`. The example shows how this interface is obtained.  
  
## Example  
  
```cpp#  
  
      IDiaDataSource* pSource;  
HRESULT hr = CoCreateInstance(CLSID_DiaSource,  
                              NULL,  
                              CLSCTX_INPROC_SERVER,  
                              IID_IDiaDataSource,  
                              (void**) &pSource);  
if (FAILED(hr))  
{  
    // Report error and exit  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)