---
title: "Constants (Debug Interface Access SDK)"
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
ms.assetid: aca4ec77-bc08-4cdd-a6ce-8d4a28ea5ea3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Constants (Debug Interface Access SDK)
These string constants can be used to identify various sections of a program debug database (PDB) file through the DIA SDK.  
  
## Constants  
 The following are declared as C/C++ macros.  
  
|Macro|Value|  
|-----------|-----------|  
|`DiaTable_Symbols`|L"Symbols"|  
|`DiaTable_Sections`|L"Sections"|  
|`DiaTable_SrcFiles`|L"SourceFiles"|  
|`DiaTable_LineNums`|L"LineNumbers"|  
|`DiaTable_SegMap`|L"SegmentMap"|  
|`DiaTable_Dbg`|L"Dbg"|  
|`DiaTable_InjSrc`|L"InjectedSource"|  
|`DiaTable_FrameData`|L"FrameData"|  
  
## Example  
 Here is an example using one of these symbols:  
  
```cpp#  
HRESULT GetSymbolTable(IDiaEnumTables *pEnumTables, IDiaTable **pTable)  
{  
    HRESULT hr;  
    VARIANT var;  
    var.vt      = VT_BSTR;  
    var.bstrVal = SysAllocString( DiaTable_Symbols );  
    hr = pEnumTables->Item( var, pTable );  
    return(hr);  
}  
```  
  
## Requirements  
 Header: dia2.h  
  
## See Also  
 [API Reference (Debug Interface Access SDK)](../vs140/Debug-Interface-Access-SDK-Reference.md)   
 [Enumerations and Structures](../vs140/Enumerations-and-Structures.md)   
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaEnumTables::Item Method](../vs140/IDiaEnumTables--Item.md)