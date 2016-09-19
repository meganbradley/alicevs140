---
title: "CWnd::OnAmbientProperty"
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
ms.assetid: 333ce640-167a-4bc9-bb75-9f35115490f4
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnAmbientProperty
The framework calls this member function to obtain ambient property values from a window that contains OLE controls.  
  
## Syntax  
  
```  
  
      virtual BOOL OnAmbientProperty(  
   COleControlSite* pSite,  
   DISPID dispid,  
   VARIANT* pvar   
);  
```  
  
#### Parameters  
 `pSite`  
 Pointer to the site of the control that requested the ambient property.  
  
 `dispid`  
 The dispatch ID of the requested ambient property.  
  
 `pvar`  
 Pointer to a caller-allocated `VARIANT` structure, through which the ambient property's value will be returned.  
  
## Return Value  
 **TRUE** if the ambient property is supported; **FALSE** if not.  
  
## Remarks  
 Override this function to alter the default ambient property values returned by an OLE control container to its controls. Any ambient property requests not handled by an overriding function should be forwarded to the base class implementation.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)