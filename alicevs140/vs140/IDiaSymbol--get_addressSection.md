---
title: "IDiaSymbol::get_addressSection"
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
ms.assetid: fe80d479-3bb5-4f55-9b62-1bd58d0a60ce
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_addressSection
Retrieves the section part of an address location. Use when the [LocationType Enumeration](../vs140/LocationType.md) is set to `LocIsStatic`.  
  
## Syntax  
  
```cpp#  
HRESULT get_addressSection (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the section part of an address location.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Remarks  
 For static members located in an external DLL, the section returned by this method may be 0 as this method relies on obtaining the virtual address of the member. Virtual addresses are valid only if the [IDiaSession::put_loadAddress](../vs140/IDiaSession--put_loadAddress.md) method in the [IDiaSession](../vs140/IDiaSession.md) interface has been called with a nonzero parameter specifying the load address of the DLL.  
  
 To get the offset part of an address, call the [IDiaSymbol::get_addressOffset](../vs140/IDiaSymbol--get_addressOffset.md) method.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v7.0|  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [LocationType Enumeration](../vs140/LocationType.md)