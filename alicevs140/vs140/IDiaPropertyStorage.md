---
title: "IDiaPropertyStorage"
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
ms.assetid: d3197a38-5973-4e56-873e-4f1b84c3f674
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaPropertyStorage
Allows you to read the persistent properties of a DIA property set.  
  
## Syntax  
  
```  
IDiaPropertyStorage : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaPropertyStorage`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaPropertyStorage::Enum](../vs140/IDiaPropertyStorage--Enum.md)|Gets a pointer to an enumerator for properties within this set.|  
|[IDiaPropertyStorage::ReadBOOL](../vs140/IDiaPropertyStorage--ReadBOOL.md)|Reads `BOOL` values in a property set.|  
|[IDiaPropertyStorage::ReadBSTR](../vs140/IDiaPropertyStorage--ReadBSTR.md)|Reads `BSTR` values in a property set.|  
|[IDiaPropertyStorage::ReadDWORD](../vs140/IDiaPropertyStorage--ReadDWORD.md)|Reads `DWORD` values in a property set.|  
|[IDiaPropertyStorage::ReadLONG](../vs140/IDiaPropertyStorage--ReadLONG.md)|Reads `LONG` values in a property set.|  
|[IDiaPropertyStorage::ReadMultiple](../vs140/IDiaPropertyStorage--ReadMultiple.md)|Reads property values in a property set.|  
|[IDiaPropertyStorage::ReadPropertyNames](../vs140/IDiaPropertyStorage--ReadPropertyNames.md)|Gets corresponding string names for given property identifiers.|  
|[IDiaPropertyStorage::ReadULONGLONG](../vs140/IDiaPropertyStorage--ReadULONGLONG.md)|Reads `ULONGLONG` values in a property set.|  
  
## Remarks  
 Each property within a property set is identified by a property identifier (ID), a four-byte `ULONG` value unique to that set. The properties exposed through the `IDiaPropertyStorage` interface correspond to the properties available in the parent interface. For example, the properties of the [IDiaSymbol](../vs140/IDiaSymbol.md) interface can be accessed by name through the `IDiaPropertyStorage` interface (note, however, that even though the property may be accessible, it does not mean the property is valid for a particular `IDiaSymbol` object).  
  
## Notes for Callers  
 Obtain this interface by calling the `QueryInterface` method on another interface. The following interfaces can be queried for the `IDiaPropertyStorage` interface:  
  
-   [IDiaSectionContrib](../vs140/IDiaSectionContrib.md)  
  
-   [IDiaSegment](../vs140/IDiaSegment.md)  
  
-   [IDiaInjectedSource](../vs140/IDiaInjectedSource.md)  
  
-   [IDiaFrameData](../vs140/IDiaFrameData.md)  
  
-   [IDiaSymbol](../vs140/IDiaSymbol.md)  
  
-   [IDiaSourceFile](../vs140/IDiaSourceFile.md)  
  
-   [IDiaLineNumber](../vs140/IDiaLineNumber.md)  
  
## Example  
 This example shows a function that displays all properties exposed by the `IDiaPropertyStorage` object. See the [IDiaEnumInjectedSources](../vs140/IDiaEnumInjectedSources.md) interface for an example of how the `IDiaPropertyStorage` interface is obtained from the [IDiaInjectedSource](../vs140/IDiaInjectedSource.md) interface.  
  
```cpp#  
void PrintPropertyStorage(IDiaPropertyStorage* pPropertyStorage)  
{  
    IEnumSTATPROPSTG* pEnumProps;  
    STATPROPSTG       prop;  
    DWORD             celt = 1;  
  
    if (pPropertyStorage->Enum(&pEnumProps) == S_OK)  
    {  
        while (pEnumProps->Next(celt, &prop, &celt) == S_OK)  
        {  
            PROPSPEC pspec = { PRSPEC_PROPID, prop.propid };  
            PROPVARIANT vt = { VT_EMPTY };  
  
            if (pPropertyStorage->ReadMultiple( 1, &pspec, &vt) == S_OK)  
            {  
                switch( vt.vt ){  
                    case VT_BOOL:  
                        wprintf( L"%32s:\t %s\n", prop.lpwstrName, vt.bVal ? L"true" : L"false" );  
                        break;  
                    case VT_I2:  
                        wprintf( L"%32s:\t %d\n", prop.lpwstrName, vt.iVal );  
                        break;  
                    case VT_UI2:  
                        wprintf( L"%32s:\t %d\n", prop.lpwstrName, vt.uiVal );  
                        break;  
                    case VT_I4:  
                        wprintf( L"%32s:\t %d\n", prop.lpwstrName, vt.intVal );  
                        break;  
                    case VT_UI4:  
                        wprintf( L"%32s:\t 0x%0x\n", prop.lpwstrName, vt.uintVal );  
                        break;  
                    case VT_UI8:  
                        wprintf( L"%32s:\t 0x%x\n", prop.lpwstrName, vt.uhVal.QuadPart );  
                        break;  
                    case VT_BSTR:  
                        wprintf( L"%32s:\t %s\n", prop.lpwstrName, vt.bstrVal );  
                        break;  
                    case VT_UNKNOWN:  
                        wprintf( L"%32s:\t %p\n", prop.lpwstrName, vt.punkVal );  
                        break;  
                    case VT_SAFEARRAY:  
                        break;  
                    default:  
                       break;  
                }  
                VariantClear((VARIANTARG*) &vt);  
            }  
        }  
        pEnumProps->Release();  
    }  
}  
```  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaSession::getEnumTables](../vs140/IDiaSession--getEnumTables.md)   
 [IDiaSectionContrib](../vs140/IDiaSectionContrib.md)   
 [IDiaSegment](../vs140/IDiaSegment.md)   
 [IDiaInjectedSource](../vs140/IDiaInjectedSource.md)   
 [IDiaFrameData](../vs140/IDiaFrameData.md)   
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [IDiaSourceFile](../vs140/IDiaSourceFile.md)   
 [IDiaLineNumber](../vs140/IDiaLineNumber.md)   
 [IDiaEnumInjectedSources](../vs140/IDiaEnumInjectedSources.md)