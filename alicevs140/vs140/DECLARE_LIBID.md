---
title: "DECLARE_LIBID"
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
ms.assetid: 44e049a5-d5c1-4a45-863e-f943e11ecf79
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_LIBID
Provides a way for ATL to obtain the *libid* of the type library.  
  
## Syntax  
  
```  
  
      DECLARE_LIBID(   
   libid    
)  
```  
  
#### Parameters  
 *libid*  
 The GUID of the type library.  
  
## Remarks  
 Use `DECLARE_LIBID` in a `CAtlModuleT`-derived class.  
  
## Example  
 Non-attributed wizard-generated ATL projects will have a sample of using this macro.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Registry Macros](../vs140/Registry-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [CAtlModuleT Class](../vs140/CAtlModuleT-Class.md)