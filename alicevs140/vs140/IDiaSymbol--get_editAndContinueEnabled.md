---
title: "IDiaSymbol::get_editAndContinueEnabled"
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
ms.assetid: cd703c64-9ff8-4654-8493-8cde9309cb22
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_editAndContinueEnabled
Retrieves a flag indicating whether the module was compiled with the [/Z7, /Zd, /Zi, /ZI (Debug Information Format)](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md) compiler switch.  
  
## Syntax  
  
```cpp#  
HRESULT get_editAndContinueEnabled (   
   BOOL* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns `TRUE` if edit-and-continue was enabled at compilation; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v7.0|  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [/Z7, /Zd, /Zi, /ZI (Debug Information Format)](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md)