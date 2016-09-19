---
title: "CAtlWinModule::ExtractCreateWndData"
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
ms.assetid: 5f66633b-f6ff-4569-ac69-862c81dbd7ae
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlWinModule::ExtractCreateWndData
This method returns a pointer to an `_AtlCreateWndData` structure.  
  
## Syntax  
  
```  
  
void* ExtractCreateWndData( );  
  
```  
  
## Return Value  
 Returns a pointer to the `_AtlCreateWndData` structure previously added with [CAtlWinModule::AddCreateWndData](../vs140/CAtlWinModule--AddCreateWndData.md), or NULL if no object is available.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlWinModule Class](../vs140/CAtlWinModule-Class.md)   
 [CAtlWinModule::AddCreateWndData](../vs140/CAtlWinModule--AddCreateWndData.md)