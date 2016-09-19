---
title: "IDebugSymbolProvider::GetTypeByName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b9d88d3b-8b75-484a-b9cc-dc8c0fbb4bc8
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugSymbolProvider::GetTypeByName
This method maps a symbol name to a symbol type.  
  
## Syntax  
  
```cpp#  
HRESULT GetTypeByName(   
   LPCOLESTR     pszClassName,  
   NAME_MATCH    nameMatch,  
   IDebugField** ppField  
);  
```  
  
```c#  
int GetTypeByName(  
   string          pszClassName,   
   NAME_MATCH      nameMatch,   
   out IDebugField ppField  
);  
```  
  
#### Parameters  
 `pszClassName`  
 [in] The symbol name.  
  
 `nameMatch`  
 [in] Selects the type of match, for example, case-sensitive. A value from the [NAME_MATCH](../vs140/NAME_MATCH.md) enumeration.  
  
 `ppField`  
 [out] Returns the symbol type as an [IDebugField](../vs140/IDebugField.md) object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method is a generic version of [IDebugSymbolProvider::GetClassTypeByName](../vs140/IDebugSymbolProvider--GetClassTypeByName.md).  
  
## See Also  
 [IDebugSymbolProvider](../vs140/IDebugSymbolProvider.md)   
 [IDebugField](../vs140/IDebugField.md)   
 [NAME_MATCH](../vs140/NAME_MATCH.md)   
 [IDebugSymbolProvider::GetClassTypeByName](../vs140/IDebugSymbolProvider--GetClassTypeByName.md)