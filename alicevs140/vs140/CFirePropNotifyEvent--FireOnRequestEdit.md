---
title: "CFirePropNotifyEvent::FireOnRequestEdit"
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
ms.assetid: b372d7a8-8d86-406b-ba2d-86beaad7ec5c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFirePropNotifyEvent::FireOnRequestEdit
Notifies all connected [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638) interfaces (on every connection point of the object) that the specified object property is about to change.  
  
## Syntax  
  
```  
  
      static HRESULT FireOnRequestEdit(  
   IUnknown* pUnk,  
   DISPID dispID   
);  
```  
  
#### Parameters  
 *pUnk*  
 [in] Pointer to the **IUnknown** of the object sending the notification.  
  
 *dispID*  
 [in] Identifier of the property about to change.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 This function is safe to call even if your control does not support connection points.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CFirePropNotifyEvent Class](../vs140/CFirePropNotifyEvent-Class.md)   
 [CFirePropNotifyEvent::FireOnChanged](../vs140/CFirePropNotifyEvent--FireOnChanged.md)   
 [CComControl::FireOnRequestEdit](../vs140/CComControl--FireOnRequestEdit.md)