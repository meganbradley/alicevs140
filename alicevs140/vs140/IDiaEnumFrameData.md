---
title: "IDiaEnumFrameData"
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
ms.assetid: 2ca7fd5a-b2fa-4b3a-9492-0263eafc435b
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumFrameData
Enumerates the various frame data elements contained in the data source.  
  
## Syntax  
  
```  
IDiaEnumFrameData : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaEnumFrameData`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaEnumFrameData::get__NewEnum](../vs140/IDiaEnumFrameData--get__NewEnum.md)|Retrieves the `IEnumVARIANT Interface` version of this enumerator.|  
|[IDiaEnumFrameData::get_Count](../vs140/IDiaEnumFrameData--get_Count.md)|Retrieves the number of frame data elements.|  
|[IDiaEnumFrameData::Item](../vs140/IDiaEnumFrameData--Item.md)|Retrieves a frame data element by means of an index.|  
|[IDiaEnumFrameData::Next](../vs140/IDiaEnumFrameData--Next.md)|Retrieves a specified number of frame data elements in the enumeration sequence.|  
|[IDiaEnumFrameData::Skip](../vs140/IDiaEnumFrameData--Skip.md)|Skips a specified number of frame data elements in an enumeration sequence.|  
|[IDiaEnumFrameData::Reset](../vs140/IDiaEnumFrameData--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[IDiaEnumFrameData::Clone](../vs140/IDiaEnumFrameData--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[IDiaEnumFrameData::frameByRVA](../vs140/IDiaEnumFrameData--frameByRVA.md)|Returns a frame by relative virtual address (RVA).|  
|[IDiaEnumFrameData::frameByVA](../vs140/IDiaEnumFrameData--frameByVA.md)|Returns a frame by virtual address (VA).|  
  
## Remarks  
  
## Notes for Callers  
 Obtain this interface from the [IDiaSession::getEnumTables](../vs140/IDiaSession--getEnumTables.md) method. See the example for details.  
  
## Example  
 This example shows how to obtain (the `GetEnumFrameData` function) and use (the `ShowFrameData` function) the `IDiaEnumFrameData` interface. See the [IDiaFrameData](../vs140/IDiaFrameData.md) interface for an example of the `PrintFrameData` function.  
  
```cpp#  
  
      IDiaEnumFrameData* GetEnumFrameData(IDiaSession *pSession)  
{  
    IDiaEnumFrameData* pUnknown    = NULL;  
    REFIID             iid         = __uuidof(IDiaEnumFrameData);  
    IDiaEnumTables*    pEnumTables = NULL;  
    IDiaTable*         pTable      = NULL;  
    ULONG              celt        = 0;  
  
    if (pSession->getEnumTables(&pEnumTables) != S_OK)  
    {  
        wprintf(L"ERROR - GetTable() getEnumTables\n");  
        return NULL;  
    }  
    while (pEnumTables->Next(1, &pTable, &celt) == S_OK && celt == 1)  
    {  
        // There is only one table that matches the given iid  
        HRESULT hr = pTable->QueryInterface(iid, (void**)&pUnknown);  
        pTable->Release();  
        if (hr == S_OK)  
        {  
            break;  
        }  
    }  
    pEnumTables->Release();  
    return pUnknown;  
}  
  
void ShowFrameData(IDiaSession *pSession)  
{  
    IDiaEnumFrameData* pEnumFrameData = GetEnumFrameData(pSession);;  
  
    if (pEnumFrameData != NULL)  
    {  
        IDiaFrameData* pFrameData;  
        ULONG celt = 0;  
  
        while(pEnumFrameData->Next(1, &pFrameData, &celt) == S_OK &&  
              celt == 1)  
        {  
            PrintFrameData(pFrameData);  
            pFrameData->Release();  
        }  
        pEnumFrameData->Release();   
    }  
}  
```  
  
## Requirements  
 **Header:** Dia2.h  
  
 **Library:** diaguids.lib  
  
 **DLL:** msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaSession::getEnumTables](../vs140/IDiaSession--getEnumTables.md)   
 [IDiaFrameData](../vs140/IDiaFrameData.md)