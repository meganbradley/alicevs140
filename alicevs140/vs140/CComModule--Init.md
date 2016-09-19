---
title: "CComModule::Init"
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
ms.assetid: 8b584e2c-d416-4d02-99e8-0a6698d1fc22
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::Init
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
      HRESULT Init(  
   _ATL_OBJMAP_ENTRY* p,  
   HINSTANCE h,  
   const GUID* plibid = NULL  
) throw( );  
```  
  
#### Parameters  
 `p`  
 [in] A pointer to an array of object map entries.  
  
 `h`  
 [in] The `HINSTANCE` passed to **DLLMain** or `WinMain`.  
  
 `plibid`  
 [in] A pointer to the LIBID of the type library associated with the project.  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 Initializes all data members.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)   
 [CComModule::Term](../vs140/CComModule--Term.md)