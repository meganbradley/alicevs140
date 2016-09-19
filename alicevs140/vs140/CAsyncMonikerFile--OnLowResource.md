---
title: "CAsyncMonikerFile::OnLowResource"
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
ms.assetid: 1f719332-6527-4749-ae7b-ce25cc824c6a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncMonikerFile::OnLowResource
Called by the moniker when resources are low.  
  
## Syntax  
  
```  
  
virtual void OnLowResource( );  
```  
  
## Remarks  
 The default implementation calls `GetBinding( )-> Abort( )`.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CAsyncMonikerFile Class](../vs140/CAsyncMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)