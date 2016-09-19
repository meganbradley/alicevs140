---
title: "IDiaSymbol::get_symbolsFileName"
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
ms.assetid: c1aa39ee-d645-431e-bf5f-0640c0998934
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_symbolsFileName
Retrieves the name of the file from which the symbols were loaded.  
  
## Syntax  
  
```cpp#  
HRESULT get_symbolsFileName (   
   BSTR* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the name of the file from which the symbols were loaded.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Remarks  
 This property is valid only for symbols with a [SymTagEnum](../vs140/SymTagEnum.md) value of `SymTagExe` that also have global scope.  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [SymTagEnum](../vs140/SymTagEnum.md)