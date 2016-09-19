---
title: "CComControlBase::DoesVerbUIActivate"
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
ms.assetid: 32fc50d6-27b0-4ee5-b083-5c8cac04a76f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::DoesVerbUIActivate
Checks that the `iVerb` parameter used by `IOleObjectImpl::DoVerb` causes the control's user interface to activate and returns **TRUE**.  
  
## Syntax  
  
```  
  
      BOOL DoesVerbUIActivate(  
   LONG iVerb   
);  
```  
  
#### Parameters  
 `iVerb`  
 Value indicating the action to be performed by `DoVerb`.  
  
## Return Value  
 Returns **TRUE** if `iVerb` equals `OLEIVERB_UIACTIVATE`, `OLEIVERB_PRIMARY`, `OLEIVERB_SHOW`, or **OLEIVERB_INPLACEACTIVATE**. Otherwise, the method returns **FALSE**.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [IOleObjectImpl::DoVerb](../vs140/IOleObjectImpl--DoVerb.md)   
 [CComControlBase::DoesVerbActivate](../vs140/CComControlBase--DoesVerbActivate.md)