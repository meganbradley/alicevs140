---
title: "IDiaEnumLineNumbers"
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
ms.assetid: cdf07b4f-19e4-4dcd-8af8-c2dbca586a7c
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumLineNumbers
Enumerates the various line numbers contained in the data source.  
  
## Syntax  
  
```  
IDiaEnumLineNumbers : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaEnumLineNumbers`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaEnumLineNumbers::get__NewEnum](../Topic/IDiaEnumLineNumbers::get__NewEnum.md)|Retrieves the [IEnumVARIANT Interface](assetId:///139e3c93-faef-4003-9079-e0e94494db3e) version of this enumerator.|  
|[IDiaEnumLineNumbers::get_Count](../vs140/IDiaEnumLineNumbers--get_Count.md)|Retrieves the number of line numbers.|  
|[IDiaEnumLineNumbers::Item](../vs140/IDiaEnumLineNumbers--Item.md)|Retrieves a line number by means of an index.|  
|[IDiaEnumLineNumbers::Next](../vs140/IDiaEnumLineNumbers--Next.md)|Retrieves a specified number of line numbers in the enumeration sequence.|  
|[IDiaEnumLineNumbers::Skip](../vs140/IDiaEnumLineNumbers--Skip.md)|Skips a specified number of line numbers in an enumeration sequence.|  
|[IDiaEnumLineNumbers::Reset](../vs140/IDiaEnumLineNumbers--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[IDiaEnumLineNumbers::Clone](../vs140/IDiaEnumLineNumbers--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
  
## Remarks  
  
## Notes for Callers  
 This interface is obtained by calling one of the following methods in the [IDiaSession](../vs140/IDiaSession.md) interface:  
  
-   [IDiaSession::findLines](../vs140/IDiaSession--findLines.md)  
  
-   [IDiaSession::findLinesByAddr](../vs140/IDiaSession--findLinesByAddr.md)  
  
-   [IDiaSession::findLinesByRVA](../vs140/IDiaSession--findLinesByRVA.md)  
  
-   [IDiaSession::findLinesByVA](../vs140/IDiaSession--findLinesByVA.md)  
  
-   [IDiaSession::findLinesByLinenum](../vs140/IDiaSession--findLinesByLinenum.md)  
  
## Example  
 This example shows how to obtain the `IDiaEnumLineNumbers` interface from a session. In this case, the example shows how to get the line number enumeration for a function (represented by `pSymbol`). For a more complete example of using line numbers, see the [IDiaLineNumber](../vs140/IDiaLineNumber.md) interface.  
  
```cpp#  
void dumpFunctionLines( IDiaSymbol* pSymbol, IDiaSession* pSession )  
{  
    ULONGLONG length = 0;  
    DWORD isect = 0;  
    DWORD offset = 0;  
    pSymbol->get_addressSection( &isect );  
    pSymbol->get_addressOffset( &offset );  
    pSymbol->get_length( &length );  
    if ( isect != 0 && length > 0 )  
    {  
        CComPtr< IDiaEnumLineNumbers > pLines;  
        if ( SUCCEEDED( pSession->findLinesByAddr(  
                                      isect,  
                                      offset,  
                                      static_cast<DWORD>( length ),  
                                      &pLines )  
                      )  
           )  
        {  
            // Do something with the enumeration  
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
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaSession::findLinesByLinenum](../vs140/IDiaSession--findLinesByLinenum.md)   
 [IDiaSession::findLinesByRVA](../vs140/IDiaSession--findLinesByRVA.md)   
 [IDiaSession::findLinesByVA](../vs140/IDiaSession--findLinesByVA.md)   
 [IDiaSession::findLines](../vs140/IDiaSession--findLines.md)   
 [IDiaSession::findLinesByAddr](../vs140/IDiaSession--findLinesByAddr.md)