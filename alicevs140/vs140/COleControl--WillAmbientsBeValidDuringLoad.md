---
title: "COleControl::WillAmbientsBeValidDuringLoad"
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
ms.assetid: 5c820021-428e-44e7-946e-5f7538dc6912
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::WillAmbientsBeValidDuringLoad
Determines whether your control should use the values of ambient properties as default values, when it is subsequently loaded from its persistent state.  
  
## Syntax  
  
```  
  
BOOL WillAmbientsBeValidDuringLoad( );  
```  
  
## Return Value  
 Nonzero indicates that ambient properties will be valid; otherwise ambient properties will not be valid.  
  
## Remarks  
 In some containers, your control may not have access to its ambient properties during the initial call to the override of `COleControl::DoPropExchange`. This is the case if the container calls [IPersistStreamInit::Load](http://msdn.microsoft.com/library/windows/desktop/ms680730) or [IPersistStorage::Load](http://msdn.microsoft.com/library/windows/desktop/ms680557) prior to calling [IOleObject::SetClientSite](http://msdn.microsoft.com/library/windows/desktop/ms684013) (that is, if it does not honor the **OLEMISC_SETCLIENTSITEFIRST** status bit).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [COleControl::GetAmbientProperty](../vs140/COleControl--GetAmbientProperty.md)