---
title: "CAtlModule::AddTermFunc"
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
ms.assetid: a86a5a97-75f6-4c5d-b810-dae868ca57d6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlModule::AddTermFunc
Adds a new function to be called when the module terminates.  
  
## Syntax  
  
```  
  
      HRESULT AddTermFunc(  
   _ATL_TERMFUNC* pFunc,  
   DWORD_PTR dw   
) throw( );  
```  
  
#### Parameters  
 *pFunc*  
 Pointer to the function to add.  
  
 `dw`  
 User-defined data, passed to the function.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlModule Class](../vs140/CAtlModule-Class.md)   
 [CAtlModule::Term](../vs140/CAtlModule--Term.md)