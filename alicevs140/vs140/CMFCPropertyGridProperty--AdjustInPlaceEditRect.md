---
title: "CMFCPropertyGridProperty::AdjustInPlaceEditRect"
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
ms.assetid: 4bb51bec-f758-460c-9c78-b6aa4027f0c9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::AdjustInPlaceEditRect
Retrieves the boundaries of the text box and optional spin button control that are used to set a property value.  
  
## Syntax  
  
```  
virtual void AdjustInPlaceEditRect(  
   CRect& rectEdit,  
   CRect& rectSpin  
);  
```  
  
#### Parameters  
 [out] `rectEdit`  
 When this method returns, a rectangle that specifies the boundaries of the text box for the property value.  
  
 [out] `rectSpin`  
 When this method returns, a rectangle that specifies the boundaries of the spin button control for the property value. Or, if the property does not support a spin button, an empty rectangle.  
  
## Remarks  
 The value area of a property consists of a text box and possibly an *option button*, such as a spin button control. This method calculates the dimensions of the text box and option button and then returns those values in the specified parameters.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CRect Class](../vs140/CRect-Class.md)   
 [CMFCPropertyGridProperty::EnableSpinControl](../vs140/CMFCPropertyGridProperty--EnableSpinControl.md)