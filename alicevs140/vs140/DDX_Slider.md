---
title: "DDX_Slider"
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
ms.topic: article
ms.assetid: d329e756-d1a0-408b-9869-f0b3592d97cb
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_Slider
The `DDX_Slider` function manages the transfer of `int` data between a slider control in a dialog box or form view and an `int` data member of the dialog box or form view object.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_Slider(  
   CDataExchange* pDX,  
   int nIDC,  
   int& value   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The resource ID of the slider control.  
  
 *value*  
 A reference to the value to be exchanged. This parameter holds or sets the slider control's current position.  
  
## Remarks  
 When `DDX_Slider` is called, *value* is set to the current position of the control's thumb, or the value receives the position, depending on the direction of the exchange.  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md). For information about slider controls, see [Using CSliderCtrl](../vs140/Using-CSliderCtrl.md).  
  
## Requirements  
 **Header:** afxdd_.h  
  
## See Also  
 [Standard Dialog Data Exchange Routines](../vs140/Standard-Dialog-Data-Exchange-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDX_FieldSlider](../vs140/DDX_FieldSlider.md)   
 [DDV_MinMaxSlider](../vs140/DDV_MinMaxSlider.md)