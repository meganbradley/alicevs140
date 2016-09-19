---
title: "RDX_TEXT"
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
ms.assetid: 47566a2e-f293-4b67-8e1c-fa83a0a0c558
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RDX_TEXT
Associates the specified registry entry with a specified member variable of type TCHAR.  
  
## Syntax  
  
```  
  
      RDX_TEXT(   
   rootkey,   
   subkey,   
   valuename,   
   member,   
   member_size    
)  
```  
  
#### Parameters  
 `rootkey`  
 The registry key root.  
  
 `subkey`  
 The registry subkey.  
  
 `valuename`  
 The registry key.  
  
 `member`  
 The member variable to associate with the specified registry entry.  
  
 `member_size`  
 The size, in bytes, of the member variable.  
  
## Remarks  
 This macro is used in conjunction with the `BEGIN_RDX_MAP` and `END_RDX_MAP` macros to associate a member variable with a given registry entry. The global function [RegistryDataExchange](../vs140/RegistryDataExchange.md), or the member function of the same name created by the `BEGIN_RDX_MAP` and `END_RDX_MAP` macros, should be used to perform exchange of data between the system registry and the member variables in the RDX map.  
  
## Requirements  
 **Header:** atlplus.h  
  
## See Also  
 [Registry Data Exchange Macros](../vs140/Registry-Data-Exchange-Macros.md)