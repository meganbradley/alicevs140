---
title: "COleControl::OnGetViewStatus"
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
ms.assetid: 36eb5169-41b3-49ad-bafb-e2fbbc74ad6a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnGetViewStatus
Called by the framework in response to a container's **IViewObjectEx::GetViewStatus** request.  
  
## Syntax  
  
```  
  
virtual DWORD OnGetViewStatus( );  
```  
  
## Return Value  
 One of the values of the **VIEWSTATUS** enumeration if successful; otherwise 0. Possible values are any combination of the following:  
  
 **VIEWSTATUS_OPAQUE**  
 Object is completely opaque. If this bit is not set, the object contains transparent parts. This bit applies only to content-related aspects and not to `DVASPECT_ICON` or `DVASPECT_DOCPRINT`.  
  
 **VIEWSTATUS_SOLIDBKGND**  
 Object has a solid background (consisting in a solid color, not a brush pattern). This bit is meaningful only if **VIEWSTATUS_OPAQUE** is set and applies only to content-related aspects and not to `DVASPECT_ICON` or `DVASPECT_DOCPRINT`.  
  
 **VIEWSTATUS_DVASPECTOPAQUE**  
 Object supports **DVASPECT_OPAQUE**. All **IViewObjectEx** methods that take a drawing aspect as a parameter can be called with this aspect.  
  
 **VIEWSTATUS_DVASPECTTRANSPARENT**  
 Object supports **DVASPECT_TRANSPARENT**. All **IViewObjectEx** methods that take a drawing aspect as a parameter can be called with this aspect.  
  
## Remarks  
 Override this function if your control uses two-pass drawing. The default implementation returns **VIEWSTATUS_OPAQUE**.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DVASPECT](http://msdn.microsoft.com/library/windows/desktop/ms690318)