---
title: "AtlWinModuleExtractCreateWndData"
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
ms.assetid: 30fe6c9b-623b-4642-ba93-81f2c23d7cad
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlWinModuleExtractCreateWndData
Call this function to extract an existing `_AtlCreateWndData` structure.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      ATLINLINE ATLAPI_(void*) AtlWinModuleExtractCreateWndData(  
_ATL_WIN_MODULE* pWinModule  
);  
```  
  
#### Parameters  
 `pWinModule`  
 Pointer to a module's [_ATL_WIN_MODULE70](../vs140/_ATL_WIN_MODULE70-Structure.md) structure.  
  
## Return Value  
 Returns a pointer to the [_AtlCreateWndData](../vs140/_AtlCreateWndData-Structure.md) structure.  
  
## Remarks  
 This function will extract an existing `_AtlCreateWndData` structure from the list referenced by a module's `_ATL_WIN_MODULE70` structure.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [WinModule Global Functions](../vs140/WinModule-Global-Functions.md)   
 [AtlWinModuleAddCreateWndData](../vs140/AtlWinModuleAddCreateWndData.md)