---
title: "CComControlBase::GetAmbientShowGrabHandles"
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
ms.assetid: 2d95e465-9210-4fe8-859a-f6d6b0cbacb6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientShowGrabHandles
Retrieves **DISPID_AMBIENT_SHOWGRABHANDLES**, a flag indicating whether the container allows the control to display grab handles for itself when active.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientShowGrabHandles(  
   BOOL& bShowGrabHandles  
);  
```  
  
#### Parameters  
 *bShowGrabHandles*  
 The property **DISPID_AMBIENT_SHOWGRABHANDLES**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)