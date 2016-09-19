---
title: "Exe"
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
ms.assetid: a781d2cf-55fe-4373-9cf1-b732864244e0
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Exe
Exe is the only symbol without either a lexical or class parent, as it represents the global scope of the .exe or .dll file. There is only one symbol with the `SymTagExe` tag per file. The [IDiaSession::get_globalScope](../vs140/IDiaSession--get_globalScope.md) method returns the symbol.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[age](../vs140/IDiaSymbol--get_age.md)|`DWORD`|Age of this executable.|  
|[guid](../vs140/IDiaSymbol--get_guid.md)|`GUID`|`GUID` of this executable.|  
|[isCTypes](../vs140/IDiaSymbol--get_isCTypes.md)|`BOOL`|`TRUE` if the symbol file associated with this executable contains C types (only in DIA SDK v8.0 or later).|  
|[isStripped](../vs140/IDiaSymbol--get_isStripped.md)|`BOOL`|`TRUE` if private symbols have been stripped from the symbol file associated with this executable (only in DIA SDK v8.0 or later).|  
|[machineType](../vs140/IDiaSymbol--get_machineType.md)|`DWORD`|Value indicating target CPU (one of the [CV_CPU_TYPE_e Enumeration](../vs140/CV_CPU_TYPE_e.md) values).|  
|[IDiaSymbol::get_name](../vs140/IDiaSymbol--get_name.md)|`BSTR`|Name of the .exe file.|  
|[signature](../vs140/IDiaSymbol--get_signature.md)|`DWORD`|Signature of the executable.|  
|[IDiaSymbol::get_symbolsFileName](../vs140/IDiaSymbol--get_symbolsFileName.md)|`BSTR`|Full path for the .exe file's .pdb or .dbg file.|  
|[symIndexId](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagExe` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
  
## See Also  
 [IDiaSession::get_globalScope](../vs140/IDiaSession--get_globalScope.md)   
 [Lexical Hierarchy of Symbol Types](../vs140/Lexical-Hierarchy-of-Symbol-Types.md)