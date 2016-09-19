---
title: "CDatabase::IsOpen"
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
ms.assetid: 1712d2dc-89c0-4026-9e21-ba58db0ae53a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::IsOpen
Call this member function to determine whether the `CDatabase` object is currently connected to a data source.  
  
## Syntax  
  
```  
  
BOOL IsOpen( ) const;  
```  
  
## Return Value  
 Nonzero if the `CDatabase` object is currently connected; otherwise 0.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::OpenEx](../vs140/CDatabase--OpenEx.md)   
 [CDatabase::Open](../vs140/CDatabase--Open.md)