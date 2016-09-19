---
title: "CConnectionPoint::OnAdvise"
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
ms.assetid: 3d742fac-3f77-41a2-89b4-9ccf48e2bc72
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CConnectionPoint::OnAdvise
Called by the framework when a connection is being established or broken.  
  
## Syntax  
  
```  
  
      virtual void OnAdvise(  
   BOOL bAdvise   
);  
```  
  
#### Parameters  
 `bAdvise`  
 **TRUE**, if a connection is being established; otherwise **FALSE**.  
  
## Remarks  
 The default implementation does nothing.  
  
 Override this function if you want notification when sinks connect to or disconnect from your connection point.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [CConnectionPoint Class](../vs140/CConnectionPoint-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)