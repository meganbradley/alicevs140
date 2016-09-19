---
title: "IDiaAddressMap::get_relativeVirtualAddressEnabled"
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
ms.assetid: 4c48af81-7148-4d9a-818e-dbe62cbfc638
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaAddressMap::get_relativeVirtualAddressEnabled
Indicates whether the calculation and use of relative virtual addresses (RVA) is enabled.  
  
## Syntax  
  
```cpp#  
HRESULT get_relativeVirtualAddressEnabled (   
   BOOL* pRetVal  
);  
```  
  
#### Parameters  
 pRetVal  
 [out] Returns `TRUE` if the calculation of RVAs is enabled.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 RVAs are enabled if the segments have been initially loaded from a PDB file. The use of RVAs can be temporarily disabled by calling the [IDiaAddressMap::put_relativeVirtualAddressEnabled](../vs140/IDiaAddressMap--put_relativeVirtualAddressEnabled.md) method.  
  
 Also, new image headers can be established by calling the [IDiaAddressMap::set_imageHeaders](../vs140/IDiaAddressMap--set_imageHeaders.md) method followed by a call to the `put_relativeVirtualAddressEnabled` method to enable use of the RVAs using the new image headers.  
  
## See Also  
 [IDiaAddressMap](../vs140/IDiaAddressMap.md)   
 [IDiaAddressMap::set_imageHeaders](../vs140/IDiaAddressMap--set_imageHeaders.md)   
 [IDiaAddressMap::put_relativeVirtualAddressEnabled](../vs140/IDiaAddressMap--put_relativeVirtualAddressEnabled.md)