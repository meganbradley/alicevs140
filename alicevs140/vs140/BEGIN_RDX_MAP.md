---
title: "BEGIN_RDX_MAP"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 95bbba6a-d550-4e36-8e6e-1c619d9e660d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_RDX_MAP
Marks the beginning of the Registry Data Exchange map.  
  
## Syntax  
  
```  
  
BEGIN_RDX_MAP  
  
```  
  
## Remarks  
 The following macros are used within the Registry Data Exchange map to read and write entries in the system registry:  
  
|Macro|Description|  
|-----------|-----------------|  
|[RDX_BINARY](../vs140/RDX_BINARY.md)|Associates the specified registry entry with a specified member variable of type BYTE.|  
|[RDX_DWORD](../vs140/RDX_DWORD.md)|Associates the specified registry entry with a specified member variable of type DWORD.|  
|[RDX_CSTRING_TEXT](../vs140/RDX_CSTRING_TEXT.md)|Associates the specified registry entry with a specified member variable of type CString.|  
|[RDX_TEXT](../vs140/RDX_TEXT.md)|Associates the specified registry entry with a specified member variable of type TCHAR.|  
  
 The global function [RegistryDataExchange](../vs140/RegistryDataExchange.md), or the member function of the same name created by the `BEGIN_RDX_MAP` and `END_RDX_MAP` macros, should be used whenever your code needs to exchange data between the system registry and the variables specified in the RDX map.  
  
## Requirements  
 **Header:** atlplus.h  
  
## See Also  
 [Registry Data Exchange Macros](../vs140/Registry-Data-Exchange-Macros.md)