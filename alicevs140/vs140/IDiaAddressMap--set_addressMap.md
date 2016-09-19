---
title: "IDiaAddressMap::set_addressMap"
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
ms.assetid: 81e82073-089b-43d5-af39-49d7a4907c7a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaAddressMap::set_addressMap
Provides an address map to support image layout translations.  
  
## Syntax  
  
```cpp#  
HRESULT set_addressMap (   
   DWORD                     cbData,  
   struct DiaAddressMapEntry data[],  
   BOOL                      imagetoSymbols  
);  
```  
  
#### Parameters  
 `cbData`  
 [in] The number of elements in the `data` parameter.  
  
 `data[]`  
 [in] An array of [DiaAddressMapEntry](../vs140/DiaAddressMapEntry.md) structures that define the translation map.  
  
 `imagetoSymbols`  
 [in] `TRUE` if the `data` parameter defines a map from the new image layout to the original layout (as described by the debug symbols). `FALSE` if `data` is a map to the new image layout taken from the original layout.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Usually, the DIA retrieves address translation maps from the program database (.pdb) file. If these values are missing, the [IDiaAddressMap::set_imageHeaders](../vs140/IDiaAddressMap--set_imageHeaders.md) method is called twice, once with the `imagetoSymbols` parameter set to `TRUE` and once with the `imagetoSymbols` parameter set to `FALSE`. Address map translations cannot be enabled using the [IDiaAddressMap::put_addressMapEnabled](../vs140/IDiaAddressMap--put_addressMapEnabled.md) method unless both translation maps are provided.  
  
## See Also  
 [DiaAddressMapEntry Structure](../vs140/DiaAddressMapEntry.md)   
 [IDiaAddressMap](../vs140/IDiaAddressMap.md)   
 [IDiaAddressMap::put_addressMapEnabled](../vs140/IDiaAddressMap--put_addressMapEnabled.md)   
 [IDiaAddressMap::set_imageHeaders](../vs140/IDiaAddressMap--set_imageHeaders.md)