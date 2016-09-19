---
title: "CSnapInItemImpl::GetScopePaneInfo"
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
ms.assetid: 5e66b318-2bef-4c4c-b02d-e0f62e07f44f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInItemImpl::GetScopePaneInfo
Call this function to retrieve the **SCOPEDATAITEM** structure of the snap-in.  
  
## Syntax  
  
```  
  
      GetScopePaneInfo (  
   SCOPEDATAITEM *pScopeDataItem   
);  
```  
  
#### Parameters  
 *pScopeDataItem*  
 [out] A pointer to the **SCOPEDATAITEM** structure of the `CSnapInItemImpl` object.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInItemImpl Class](../Topic/CSnapInItemImpl%20Class.md)