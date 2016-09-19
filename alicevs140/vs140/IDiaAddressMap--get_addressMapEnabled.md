---
title: "IDiaAddressMap::get_addressMapEnabled"
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
ms.assetid: 6183dc5e-befa-4e5a-ae5a-f4aa24f3ed9e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaAddressMap::get_addressMapEnabled
Indicates whether an address map has been established for a particular session.  
  
## Syntax  
  
```cpp#  
HRESULT get_addressMapEnabled (   
   BOOL* pRetVal  
);  
```  
  
#### Parameters  
 pRetVal  
 [out] Returns `TRUE` if the address mapping is enabled.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Executable post-processors sometimes update the executable. DIA contains a mechanism to support the translation of symbols to the new layout.  
  
 Client applications can set the address map for a particular session by getting the [IDiaAddressMap](../vs140/IDiaAddressMap.md) interface from the [IDiaSession](../vs140/IDiaSession.md) interface and calling the [IDiaAddressMap::set_addressMap](../vs140/IDiaAddressMap--set_addressMap.md) method followed by a call to the [IDiaAddressMap::put_addressMapEnabled](../vs140/IDiaAddressMap--put_addressMapEnabled.md) method. The `get_addressMapEnabled` method returns the results of calling the `put_addressMapEnabled` method.  
  
## See Also  
 [IDiaAddressMap](../vs140/IDiaAddressMap.md)   
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaAddressMap::set_addressMap](../vs140/IDiaAddressMap--set_addressMap.md)   
 [IDiaAddressMap::put_addressMapEnabled](../vs140/IDiaAddressMap--put_addressMapEnabled.md)