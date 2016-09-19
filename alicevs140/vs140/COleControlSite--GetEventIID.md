---
title: "COleControlSite::GetEventIID"
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
ms.assetid: 306558fb-3a10-4f29-9d18-b7b73dec1266
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::GetEventIID
Retrieves a pointer to the control's default event interface.  
  
## Syntax  
  
```  
  
      BOOL GetEventIID(  
   IID* piid   
);  
```  
  
#### Parameters  
 `piid`  
 A pointer to an interface ID.  
  
## Return Value  
 Nonzero if successful, otherwise 0. If successful, `piid` contains the interface ID for the control's default event interface.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)