---
title: "COleControl::DoSuperclassPaint"
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
ms.assetid: 2581232d-90d1-4d01-af9f-5fb75aa21e19
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::DoSuperclassPaint
Redraws an OLE control that has been subclassed from a Windows control.  
  
## Syntax  
  
```  
  
      void DoSuperclassPaint(  
   CDC* pDC,  
   const CRect& rcBounds   
);  
```  
  
#### Parameters  
 `pDC`  
 A pointer to the device context of the control container.  
  
 `rcBounds`  
 The area in which the control is to be drawn.  
  
## Remarks  
 Call this function to properly handle the painting of a nonactive OLE control. This function should only be used if the OLE control subclasses a Windows control and should be called in the `OnDraw` function of your control.  
  
 For more information on this function and subclassing a Windows control, see the article [ActiveX Controls: Subclassing a Windows Control](../vs140/MFC-ActiveX-Controls--Subclassing-a-Windows-Control.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnDraw](../vs140/COleControl--OnDraw.md)