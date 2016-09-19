---
title: "CComControlBase::OnDrawAdvanced"
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
ms.assetid: a8e59a81-50f7-4472-a341-dd5909fec133
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::OnDrawAdvanced
The default `OnDrawAdvanced` prepares a normalized device context for drawing, then calls your control class's `OnDraw` method.  
  
## Syntax  
  
```  
  
      virtual HRESULT OnDrawAdvanced(  
   ATL_DRAWINFO& di   
);  
```  
  
#### Parameters  
 `di`  
 A reference to the [ATL_DRAWINFO](../vs140/ATL_DRAWINFO-Structure.md) structure that contains drawing information such as the draw aspect, the control bounds, and whether the drawing is optimized or not.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 Override this method if you want to accept the device context passed by the container without normalizing it.  
  
 See [CComControlBase::OnDraw](../vs140/CComControlBase--OnDraw.md) for more details.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)