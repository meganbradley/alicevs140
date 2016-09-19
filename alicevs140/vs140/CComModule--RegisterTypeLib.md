---
title: "CComModule::RegisterTypeLib"
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
ms.assetid: ae43e8b4-1d82-4fe8-8013-8a933fe92bb3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::RegisterTypeLib
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
      HRESULT RegisterTypeLib( ) throw( );   
HRESULT RegisterTypeLib(  
   LPCTSTR lpszIndex   
) throw( );  
```  
  
#### Parameters  
 `lpszIndex`  
 [in] String in the format `"\\N"`, where `N` is the integer index of the TYPELIB resource.  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 Adds information about a type library to the system registry.  
  
 If the module instance contains multiple type libraries, use the second version of this method to specify which type library should be used.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)