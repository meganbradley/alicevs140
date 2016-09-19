---
title: "IDiaSymbol::get_frontEndMinor"
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
ms.assetid: 40792153-827c-4859-be7c-6aa16d5abab6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_frontEndMinor
Retrieves the front end minor version number.  
  
## Syntax  
  
```cpp#  
HRESULT get_frontEndMinor (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the front.end minor version number.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Remarks  
 A compiler is typically composed of two primary elements: the front end (the parser), which handles parsing the source code into an intermediate form, and a back end (code generator), which converts the intermediate form into assembly. It is not uncommon for the front end to have a different version than the back end.  
  
 A front end or back end version number is composed of three parts: <major\>.<minor\>.<build\>, where <major\> is the major version number, <minor\> is the minor version number, and <build\> is the build number. For example, 13.10.3077.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v7.0|  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)