---
title: "IDiaEnumSectionContribs::Item"
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
ms.assetid: 63a28f23-0ca0-44a7-b11b-ca0206d642a0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumSectionContribs::Item
Retrieves section contributions by means of an index.  
  
## Syntax  
  
```cpp#  
HRESULT Item (   
   DWORD                index,  
   IDiaSectionContrib** section  
);  
```  
  
#### Parameters  
 index  
 [in] Index of the [IDiaSectionContrib](../vs140/IDiaSectionContrib.md) object to be retrieved. The index is in the range 0 to `count`-1, where `count` is returned by the [IDiaEnumSectionContribs::get_Count](../vs140/IDiaEnumSectionContribs--get_Count.md) method.  
  
 section  
 [out] Returns an [IDiaSectionContrib](../vs140/IDiaSectionContrib.md) object representing the desired section contribution.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumSectionContribs::get_Count](../vs140/IDiaEnumSectionContribs--get_Count.md)   
 [IDiaSectionContrib](../vs140/IDiaSectionContrib.md)