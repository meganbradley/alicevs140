---
title: "IDiaEnumTables::Item"
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
ms.assetid: d65ab262-10c6-48ce-95a3-b5e4cb2c85af
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumTables::Item
Retrieves a table by means of an index or name.  
  
## Syntax  
  
```cpp#  
HRESULT Item (   
   VARIANT     index,  
   IDiaTable** table  
);  
```  
  
#### Parameters  
 `index`  
 [in] Index or name of the [IDiaTable](../vs140/IDiaTable.md) to be retrieved. If an integer variant is used, it must be in the range 0 to `count`-1, where `count` is as returned by the [IDiaEnumTables::get_Count](../vs140/IDiaEnumTables--get_Count.md) method.  
  
 `table`  
 [out] Returns an [IDiaTable](../vs140/IDiaTable.md) object representing the desired table.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 If a string variant is specified, then the string names a particular table. The name should be one of the table names as defined in [Constants (Debug Interface Access SDK)](../vs140/Constants--Debug-Interface-Access-SDK-.md).  
  
## Example  
  
```cpp#  
VARIANT var;  
var.vt = VT_BSTR;  
var.bstrVal = SysAllocString(DiaTable_Symbols );  
IDiaTable* pTable;  
pEnumTables->Item( var, &pTable );  
```  
  
## See Also  
 [IDiaEnumTables](../vs140/IDiaEnumTables.md)   
 [IDiaTable](../vs140/IDiaTable.md)   
 [IDiaEnumTables::get_Count](../vs140/IDiaEnumTables--get_Count.md)   
 [Constants (Debug Interface Access SDK)](../vs140/Constants--Debug-Interface-Access-SDK-.md)