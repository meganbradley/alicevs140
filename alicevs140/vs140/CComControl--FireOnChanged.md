---
title: "CComControl::FireOnChanged"
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
ms.assetid: 94db6bed-246c-4205-a362-82cda3ba1e1a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControl::FireOnChanged
Notifies the container's sink that a control property has changed.  
  
## Syntax  
  
```  
  
      HRESULT FireOnChanged(  
   DISPID dispID   
);  
```  
  
#### Parameters  
 *dispID*  
 [in] Identifier of the property that has changed.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Remarks  
 If your control class derives from [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638), this method calls [CFirePropNotifyEvent::FireOnChanged](../vs140/CFirePropNotifyEvent--FireOnChanged.md) to notify all connected `IPropertyNotifySink` interfaces that the specified control property has changed. If your control class does not derive from `IPropertyNotifySink`, this method returns `S_OK`.  
  
 This method is safe to call even if your control doesn't support connection points.  
  
## Example  
 [!CODE [NVC_ATL_COM#17](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#17)]  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControl Class](../vs140/CComControl-Class.md)   
 [CComControl::FireOnRequestEdit](../vs140/CComControl--FireOnRequestEdit.md)