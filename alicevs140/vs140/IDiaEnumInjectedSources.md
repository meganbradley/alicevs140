---
title: "IDiaEnumInjectedSources"
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
ms.assetid: f97e2392-22e1-48da-b7ce-ad94c8b684b0
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumInjectedSources
Enumerate the various injected sources contained in the data source.  
  
## Syntax  
  
```  
IDiaEnumInjectedSources : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaEnumInjectedSources`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaEnumInjectedSources::get__NewEnum](../vs140/IDiaEnumInjectedSources--get__NewEnum.md)|Retrieves the [IEnumVARIANT Interface](assetId:///139e3c93-faef-4003-9079-e0e94494db3e) version of this enumerator.|  
|[IDiaEnumInjectedSources::get_Count](../vs140/IDiaEnumInjectedSources--get_Count.md)|Retrieves the number of injected sources.|  
|[IDiaEnumInjectedSources::Item](../vs140/IDiaEnumInjectedSources--Item.md)|Retrieves an injected source by means of an index.|  
|[IDiaEnumInjectedSources::Next](../vs140/IDiaEnumInjectedSources--Next.md)|Retrieves a specified number of injected sources in the enumeration sequence.|  
|[IDiaEnumInjectedSources::Skip](../vs140/IDiaEnumInjectedSources--Skip.md)|Skips a specified number of injected sources in an enumeration sequence.|  
|[IDiaEnumInjectedSources::Reset](../vs140/IDiaEnumInjectedSources--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[IDiaEnumInjectedSources::Clone](../vs140/IDiaEnumInjectedSources--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
  
## Remarks  
  
## Notes for Callers  
 This interface is obtained by calling the [IDiaSession::findInjectedSource](../vs140/IDiaSession--findInjectedSource.md) method with the name of a specific source file or by calling the [IDiaSession::getEnumTables](../vs140/IDiaSession--getEnumTables.md) method with the GUID of the `IDiaEnumInjectedSources` interface.  
  
## Example  
 This example shows how to obtain (the `GetEnumInjectedSources` function) and use (the `DumpAllInjectedSources` function) the `IDiaEnumInjectedSources` interface. See the [IDiaPropertyStorage](../vs140/IDiaPropertyStorage.md) interface for an implementation of the `PrintPropertyStorage` function. For an alternative output, see the [IDiaInjectedSource](../vs140/IDiaInjectedSource.md) interface.  
  
```cpp#  
  
IDiaEnumInjectedSources* GetEnumInjectedSources(IDiaSession *pSession)  
{  
    IDiaEnumInjectedSources* pUnknown    = NULL;  
    REFIID                   iid         = __uuidof(IDiaEnumInjectedSources);  
    IDiaEnumTables*          pEnumTables = NULL;  
    IDiaTable*               pTable      = NULL;  
    ULONG                    celt        = 0;  
  
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
  
void DumpAllInjectedSources( IDiaSession* pSession)  
{  
    IDiaEnumInjectedSources* pEnumInjSources;  
  
    pEnumInjSources = GetEnumInjectedSources(pSession);  
    if (pEnumInjSources != NULL)  
    {  
        IDiaInjectedSource* pInjSource;  
        ULONG celt = 0;  
  
        while(pEnumInjSources->Next(1, &pInjSource, &celt) == S_OK &&  
              celt == 1)  
        {  
            IDiaPropertyStorage *pPropertyStorage;  
            if (pInjSource->QueryInterface(__uuidof(IDiaPropertyStorage),  
                                           (void **)&pPropertyStorage) == S_OK)  
            {  
                PrintPropertyStorage(pPropertyStorage);  
                pPropertyStorage->Release();  
            }  
            pInjSource->Release();  
        }  
        pEnumInjSources->Release();  
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaSession::findInjectedSource](../vs140/IDiaSession--findInjectedSource.md)   
 [IDiaSession::getEnumTables](../vs140/IDiaSession--getEnumTables.md)   
 [IDiaPropertyStorage](../vs140/IDiaPropertyStorage.md)   
 [IDiaInjectedSource](../vs140/IDiaInjectedSource.md)