---
title: "IDiaSymbol::get_type"
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
ms.assetid: 1c6a4176-dd4e-4c22-8b8f-0e559fc078ba
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_type
Retrieves the symbol that represents the type for this symbol.  
  
## Syntax  
  
```cpp#  
HRESULT get_type (   
   IDiaSymbol** pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns an [IDiaSymbol](../vs140/IDiaSymbol.md) object that represents the type of this symbol.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Remarks  
 To determine the type a symbol has, you must call this method and examine the resulting [IDiaSymbol](../vs140/IDiaSymbol.md) object. Note that it is possible for a symbol to not have a type. For example, the name of a structure has no type but it might have children symbols (use the [IDiaSymbol::findChildren](../vs140/IDiaSymbol--findChildren.md) method to examine those children).  
  
## Example  
  
```cpp#  
IDiaSymbol*         pType;  
CComPtr<IDiaSymbol> pBaseType;  
if (SUCCEEDED(pType->get_type( &pBaseType ))) {  
    BasicType btBaseType;  
    if (SUCCEEDED(pBaseType->get_baseType((DWORD *)&btBaseType))) {  
        // Do something with basic type.  
    }  
}  
```  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [IDiaSymbol::get_baseType](../vs140/IDiaSymbol--get_baseType.md)   
 [IDiaSymbol::findChildren](../vs140/IDiaSymbol--findChildren.md)