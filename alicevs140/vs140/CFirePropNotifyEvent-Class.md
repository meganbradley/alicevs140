---
title: "CFirePropNotifyEvent Class"
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
ms.assetid: eb7a563e-6bce-4cdf-8d20-8c6a5307781b
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFirePropNotifyEvent Class
This class provides methods for notifying the container's sink regarding control property changes.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CFirePropNotifyEvent  
  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CFirePropNotifyEvent::FireOnChanged](../vs140/CFirePropNotifyEvent--FireOnChanged.md)|(Static) Notifies the container's sink that a control property has changed.|  
|[CFirePropNotifyEvent::FireOnRequestEdit](../vs140/CFirePropNotifyEvent--FireOnRequestEdit.md)|(Static) Notifies the container's sink that a control property is about to change.|  
  
## Remarks  
 `CFirePropNotifyEvent` has two methods that notify the container's sink that a control property has changed or is about to change.  
  
 If the class implementing your control is derived from `IPropertyNotifySink`, the `CFirePropNotifyEvent` methods are invoked when you call `FireOnRequestEdit` or `FireOnChanged`. If your control class is not derived from `IPropertyNotifySink`, calls to these functions return `S_OK`.  
  
 For more information about creating controls, see the [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md).  
  
## Requirements  
 **Header:** atlctl.h  
  
##  <a name="cfirepropnotifyevent__fireonchanged"></a>  CFirePropNotifyEvent::FireOnChanged  
 Notifies all connected [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638) interfaces (on every connection point of the object) that the specified object property has changed.  
  
```  
  
static HRESULT FireOnChanged(  
      IUnknown*  pUnk,  
   DISPID  dispID  
   );  
  
```  
  
### Parameters  
 *pUnk*  
 [in] Pointer to the **IUnknown** of the object sending the notification.  
  
 *dispID*  
 [in] Identifier of the property that has changed.  
  
### Return Value  
 One of the standard `HRESULT` values.  
  
### Remarks  
 This function is safe to call even if your control does not support connection points.  
  
##  <a name="cfirepropnotifyevent__fireonrequestedit"></a>  CFirePropNotifyEvent::FireOnRequestEdit  
 Notifies all connected [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638) interfaces (on every connection point of the object) that the specified object property is about to change.  
  
```  
  
static HRESULT FireOnRequestEdit(  
      IUnknown*  pUnk,  
   DISPID  dispID  
   );  
  
```  
  
### Parameters  
 *pUnk*  
 [in] Pointer to the **IUnknown** of the object sending the notification.  
  
 *dispID*  
 [in] Identifier of the property about to change.  
  
### Return Value  
 One of the standard `HRESULT` values.  
  
### Remarks  
 This function is safe to call even if your control does not support connection points.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)