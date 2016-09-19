---
title: "COleControl::GetControlSize"
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
ms.assetid: 2c21918a-e9ff-47a7-a5d0-6af4e1496d0a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetControlSize
Retrieves the size of the OLE control window.  
  
## Syntax  
  
```  
  
      void GetControlSize(  
   int* pcx,  
   int* pcy   
);  
```  
  
#### Parameters  
 *pcx*  
 Specifies the width of the control in pixels.  
  
 *pcy*  
 Specifies the height of the control in pixels.  
  
## Remarks  
 Note that all coordinates for control windows are relative to the upper-left corner of the control.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetRectInContainer](../vs140/COleControl--GetRectInContainer.md)   
 [COleControl::SetControlSize](../vs140/COleControl--SetControlSize.md)