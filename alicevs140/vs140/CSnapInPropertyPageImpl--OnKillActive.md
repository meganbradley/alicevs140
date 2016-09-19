---
title: "CSnapInPropertyPageImpl::OnKillActive"
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
ms.assetid: 7399cf8e-c0b1-47ba-ae81-d28485d1853a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInPropertyPageImpl::OnKillActive
This member function is called when the page is no longer the active page.  
  
## Syntax  
  
```  
  
BOOL OnKillActive( );  
  
```  
  
## Return Value  
 Nonzero if data was updated successfully; otherwise 0.  
  
## Remarks  
 Override this member function to perform special data validation tasks.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInPropertyPageImpl Class](../vs140/CSnapInPropertyPageImpl-Class.md)