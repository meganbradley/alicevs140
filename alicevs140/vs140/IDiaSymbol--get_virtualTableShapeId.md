---
title: "IDiaSymbol::get_virtualTableShapeId"
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
ms.assetid: cbee9944-817a-4805-9c08-fac8e0da58b7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_virtualTableShapeId
Retrieves the virtual table shape symbol identifier of the symbol.  
  
## Syntax  
  
```cpp#  
HRESULT get_virtualTableShapeId (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the virtual table shape symbol ID of the symbol.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Remarks  
 The identifier is a unique value created by the DIA SDK to mark all symbols as unique.  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)