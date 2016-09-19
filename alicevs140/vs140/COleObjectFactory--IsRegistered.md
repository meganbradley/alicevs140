---
title: "COleObjectFactory::IsRegistered"
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
ms.assetid: 6ce20d7d-f475-4bff-a4e2-1011cf925a72
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleObjectFactory::IsRegistered
Returns a nonzero value if the factory is registered with the OLE system DLLs.  
  
## Syntax  
  
```  
  
virtual BOOL IsRegistered( ) const;  
```  
  
## Return Value  
 Nonzero if the factory is registered; otherwise 0.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleObjectFactory Class](../vs140/COleObjectFactory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleObjectFactory::Register](../vs140/COleObjectFactory--Register.md)   
 [COleObjectFactory::Revoke](../vs140/COleObjectFactory--Revoke.md)