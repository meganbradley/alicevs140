---
title: "IDiaSymbol::get_classParent"
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
ms.assetid: 99db875a-caae-4d60-ae70-64bc8a9f6fba
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_classParent
Retrieves a reference to the class parent of the symbol.  
  
## Syntax  
  
```cpp#  
HRESULT get_classParent (   
   IDiaSymbol** pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns an [IDiaSymbol](../vs140/IDiaSymbol.md) object that represents the class parent of the symbol.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v7.0|  
  
## Remarks  
 The types of symbols that can be class parents are documented in [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md).  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)