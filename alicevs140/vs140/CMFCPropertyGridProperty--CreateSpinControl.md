---
title: "CMFCPropertyGridProperty::CreateSpinControl"
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
ms.assetid: bb03f7e7-5d16-4c3e-81fd-a27fafbb3170
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::CreateSpinControl
Called by the framework to create an editable spin button control.  
  
## Syntax  
  
```  
virtual CSpinButtonCtrl* CreateSpinControl(  
   CRect rectSpin   
);  
```  
  
#### Parameters  
 [in] `rectSpin`  
 A rectangle that defines where the editable spin button control is created.  
  
## Return Value  
 A pointer to a new [CMFCSpinButtonCtrl](../vs140/CMFCSpinButtonCtrl-Class.md) object that is cast as a pointer to a [CSpinButtonCtrl](../vs140/CSpinButtonCtrl-Class.md) object.  
  
## Remarks  
 Call the [CMFCPropertyGridProperty::EnableSpinControl](../vs140/CMFCPropertyGridProperty--EnableSpinControl.md) method to display an editable spin button control at the right edge of the property.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)