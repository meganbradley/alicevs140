---
title: "IDiaTable"
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
ms.assetid: c99a2c44-7b72-4e3c-b963-25fe3df3a555
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaTable
Enumerates a DIA data source table.  
  
## Syntax  
  
```  
IDiaTable : IEnumUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaTable`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaTable::get__NewEnum](../vs140/IDiaTable--get__NewEnum.md)|Retrieves the [IEnumVARIANT Interface](assetId:///139e3c93-faef-4003-9079-e0e94494db3e) version of this enumerator.|  
|[IDiaTable::get_name](../vs140/IDiaTable--get_name.md)|Retrieves the name of the table.|  
|[IDiaTable::get_Count](../vs140/IDiaTable--get_Count.md)|Retrieves the number of items in the table.|  
|[IDiaTable::Item](../vs140/IDiaTable--Item.md)|Retrieves a reference to a particular entry index.|  
  
## Remarks  
 This interface implements the `IEnumUnknown` enumeration methods in the Microsoft.VisualStudio.OLE.Interop namespace. The `IEnumUnknown` enumeration interface is much more efficient for iterating over the table contents than the [IDiaTable::get_Count](../vs140/IDiaTable--get_Count.md) and [IDiaTable::Item](../vs140/IDiaTable--Item.md) methods.  
  
 The interpretation of the `IUnknown` interface returned from either the `IDiaTable::Item` method or the `Next` method (in the Microsoft.VisualStudio.OLE.Interop namespace) is dependent on the type of table. For example, if the `IDiaTable` interface represents a list of injected sources, the `IUnknown` interface should be queried for the [IDiaInjectedSource](../vs140/IDiaInjectedSource.md) interface.  
  
## Notes for Callers  
 Obtain this interface by calling the [IDiaEnumTables::Item](../vs140/IDiaEnumTables--Item.md) or [IDiaEnumTables::Next](../vs140/IDiaEnumTables--Next.md) methods.  
  
 The following interfaces are implemented with the `IDiaTable` interface (that is, you can query the `IDiaTable` interface for one of the following interfaces):  
  
-   [IDiaEnumSymbols](../vs140/IDiaEnumSymbols.md)  
  
-   [IDiaEnumSourceFiles](../vs140/IDiaEnumSourceFiles.md)  
  
-   [IDiaEnumLineNumbers](../vs140/IDiaEnumLineNumbers.md)  
  
-   [IDiaEnumSectionContribs](../vs140/IDiaEnumSectionContribs.md)  
  
-   [IDiaEnumSegments](../vs140/IDiaEnumSegments.md)  
  
-   [IDiaEnumInjectedSources](../vs140/IDiaEnumInjectedSources.md)  
  
-   [IDiaEnumFrameData](../vs140/IDiaEnumFrameData.md)  
  
## Example  
 The first function, `ShowTableNames`, displays the names of all the tables in the session. The second function, `GetTable`, searches all of the tables for a table that implements a specified interface. The third function, `UseTable`, shows how to use the `GetTable` function.  
  
> [!NOTE]
>  `CDiaBSTR` is a class that wraps a `BSTR` and automatically handles freeing the string when the instantiation goes out of scope.  
  
```cpp#  
void ShowTableNames(IDiaSession *pSession)  
{  
    CComPtr<IDiaEnumTables> pTables;  
    if ( FAILED( psession->getEnumTables( &pTables ) ) )  
    {  
        Fatal( "getEnumTables" );  
    }  
    CComPtr< IDiaTable > pTable;  
    while ( SUCCEEDED( hr = pTables->Next( 1, &pTable, &celt ) )  
            && celt == 1 )  
    {  
        CDiaBSTR bstrTableName;  
        if ( pTable->get_name( &bstrTableName ) != 0 )  
        {  
            Fatal( "get_name" );  
        }  
        printf( "Found table: %ws\n", bstrTableName );  
    }  
  
// Searches the list of all tables for a table that supports  
// the specified interface.  Use this function to obtain an  
// enumeration interface.  
HRESULT GetTable(IDiaSession* pSession,  
                 REFIID       iid,  
                 void**       ppUnk)  
{  
    CComPtr<IDiaEnumTables> pEnumTables;  
    HRESULT hResult;  
  
    if (FAILED(pSession->getEnumTables(&pEnumTables)))  
        Fatal("getEnumTables");  
  
    CComPtr<IDiaTable> pTable;  
    ULONG celt = 0;  
    while (SUCCEEDED(hResult = pEnumTables->Next(1, &pTable, &celt)) &&  
           celt == 1)  
    {  
        if (pTable->QueryInterface(iid, (void**)ppUnk) == S_OK)  
        {  
            return S_OK;  
        }  
        pTable = NULL;  
    }  
  
    if (FAILED(hResult))  
        Fatal("EnumTables->Next");  
  
    return E_FAIL;  
}  
  
// This function shows how to use the GetTable function.  
void UseTable(IDiaSession *pSession)  
{  
    CComPtr<IDiaEnumSegments> pEnumSegments;  
    if (SUCCEEDED(GetTable(pSession, __uuidof(IDiaEnumSegments), &pEnumSegments)))  
    {  
        // Do something with pEnumSegments.  
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaEnumTables](../vs140/IDiaEnumTables.md)   
 [IDiaEnumTables::Item](../vs140/IDiaEnumTables--Item.md)   
 [IDiaEnumTables::Next](../vs140/IDiaEnumTables--Next.md)