---
title: "COleControl::OnSetExtent"
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
ms.assetid: 0f75031d-b127-4fcc-812b-babf9055df4e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnSetExtent
Called by the framework when the control's extent needs to be changed, as a result of a call to [IOleObject::SetExtent](http://msdn.microsoft.com/library/windows/desktop/ms694330).  
  
## Syntax  
  
```  
  
      virtual BOOL OnSetExtent(  
   LPSIZEL lpSizeL   
);  
```  
  
#### Parameters  
 `lpSizeL`  
 A pointer to the **SIZEL** structure that uses long integers to represent the width and height of the control, expressed in **HIMETRIC** units.  
  
## Return Value  
 Nonzero if the size change was accepted; otherwise 0.  
  
## Remarks  
 The default implementation handles the resizing of the control's extent. If the control is in-place active, a call to the container's **OnPosRectChanged** is then made.  
  
 Override this function to alter the default resizing of your control.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)