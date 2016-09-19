---
title: "CComControlBase::DoesVerbActivate"
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
ms.assetid: 8ee7bfe0-6844-4fce-8e9d-5425b03fcc18
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::DoesVerbActivate
Checks that the `iVerb` parameter used by `IOleObjectImpl::DoVerb` either activates the control's user interface (`iVerb` equals `OLEIVERB_UIACTIVATE`), defines the action taken when the user double-clicks the control (`iVerb` equals `OLEIVERB_PRIMARY`), displays the control (`iVerb` equals `OLEIVERB_SHOW`), or activates the control (`iVerb` equals **OLEIVERB_INPLACEACTIVATE**).  
  
## Syntax  
  
```  
  
      BOOL DoesVerbActivate(  
   LONG iVerb   
);  
```  
  
#### Parameters  
 `iVerb`  
 Value indicating the action to be performed by `DoVerb`.  
  
## Return Value  
 Returns **TRUE** if `iVerb` equals `OLEIVERB_UIACTIVATE`, `OLEIVERB_PRIMARY`, `OLEIVERB_SHOW`, or **OLEIVERB_INPLACEACTIVATE**; otherwise, returns **FALSE**.  
  
## Remarks  
 You can override this method to define your own activation verb.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [IOleObjectImpl::DoVerb](../vs140/IOleObjectImpl--DoVerb.md)   
 [CComControlBase::DoesVerbUIActivate](../vs140/CComControlBase--DoesVerbUIActivate.md)