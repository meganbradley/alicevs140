---
title: "CAtlWinModule::AddCreateWndData"
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
ms.assetid: dfef9bd1-409c-44bc-aac3-ef86bfc83570
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlWinModule::AddCreateWndData
This method initializes and adds an `_AtlCreateWndData` structure.  
  
## Syntax  
  
```  
  
      void AddCreateWndData(  
   _AtlCreateWndData* pData,  
   void* pObject   
);  
```  
  
#### Parameters  
 `pData`  
 Pointer to the `_AtlCreateWndData` structure to be initialized and added to the current module.  
  
 `pObject`  
 Pointer to an object's **this** pointer.  
  
## Remarks  
 This method calls [AtlWinModuleAddCreateWndData](../vs140/AtlWinModuleAddCreateWndData.md) which initializes an [_AtlCreateWndData](../vs140/_AtlCreateWndData-Structure.md) structure. This structure will store the **this** pointer, used to obtain the class instance in window procedures.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlWinModule Class](../vs140/CAtlWinModule-Class.md)   
 [CAtlWinModule::ExtractCreateWndData](../vs140/CAtlWinModule--ExtractCreateWndData.md)