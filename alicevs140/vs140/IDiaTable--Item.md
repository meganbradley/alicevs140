---
title: "IDiaTable::Item"
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
ms.assetid: eae11b26-4807-400c-be25-e85bbc0c6b20
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaTable::Item
Retrieves a reference to the specified entry in the table.  
  
## Syntax  
  
```cpp#  
HRESULT Item (   
   DWORD      index,  
   IUnknown** element  
);  
```  
  
#### Parameters  
 `index`  
 [in] The index of the table entry in the range 0 to `count`-1, where `count` is returned by the [IDiaTable::get_Count](../vs140/IDiaTable--get_Count.md)method.  
  
 `element`  
 [out] Returns an `IUnknown` object that represents the specified table entry.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 A table represents a collection of objects. Depending on those objects, the element parameter can be cast to the appropriate interface. For example, if a table contains [IDiaSegment](../vs140/IDiaSegment.md) objects, then the element parameter can be cast to the `IDiaSegment` interface.  
  
 It is a more common approach to call the `QueryInterface` method in the [IDiaTable](../vs140/IDiaTable.md) interface for the appropriate enumerator interface and use the enumerator's specific methods to access the table contents. See the [IDiaEnumInjectedSources](../vs140/IDiaEnumInjectedSources.md) interface for an example.  
  
## See Also  
 [IDiaTable](../vs140/IDiaTable.md)   
 [IDiaTable::get_Count](../vs140/IDiaTable--get_Count.md)   
 [IDiaSegment](../vs140/IDiaSegment.md)   
 [IDiaEnumInjectedSources](../vs140/IDiaEnumInjectedSources.md)