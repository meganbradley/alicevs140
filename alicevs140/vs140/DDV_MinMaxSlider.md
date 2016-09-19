---
title: "DDV_MinMaxSlider"
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
ms.assetid: 19f03fba-facd-473f-b644-4fac5614e606
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDV_MinMaxSlider
Call `DDV_MinMaxSlider` to verify that the value in the control associated with *value* falls between `minVal` and `maxVal`.  
  
## Syntax  
  
```  
  
      void AFXAPI DDV_MinMaxSlider(  
   CDataExchange* pDX,  
   DWORD value,  
   DWORD minVal,  
   DWORD maxVal   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 *value*  
 A reference to the value to be validated. This parameter holds or sets the slider control's current thumb position.  
  
 `minVal`  
 Minimum value allowed.  
  
 `maxVal`  
 Maximum value allowed.  
  
## Remarks  
 For more information about DDV, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md). For information about slider controls, see [Using CSliderCtrl](../vs140/Using-CSliderCtrl.md).  
  
## Requirements  
 **Header:** afxdd_.h  
  
## See Also  
 [Standard Dialog Data Validation Routines](../vs140/Standard-Dialog-Data-Validation-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDX_Slider](../vs140/DDX_Slider.md)   
 [DDX_FieldSlider](../vs140/DDX_FieldSlider.md)