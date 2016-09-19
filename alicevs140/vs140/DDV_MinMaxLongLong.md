---
title: "DDV_MinMaxLongLong"
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
ms.assetid: cd5eeeaa-a403-46d8-97c8-990a5b05749c
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDV_MinMaxLongLong
Call `DDV_MinMaxLongLong` to verify that the value in the control associated with *value* falls between `minVal` and `maxVal`.  
  
## Syntax  
  
```  
  
      void AFXAPI DDV_MinMaxLongLong(  
   CDataExchange* pDX,  
   LONGLONG value,  
   LONGLONG minVal,  
   LONGLONG maxVal   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 *value*  
 A reference to a member variable of the dialog box, form view, or control view object with which data is validated.  
  
 `minVal`  
 Minimum value (of type **LONGLONG**) allowed.  
  
 `maxVal`  
 Maximum value (of type **LONGLONG**) allowed.  
  
## Remarks  
 For more information about DDV, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## Requirements  
 **Header:** afxdd_.h  
  
## See Also  
 [Standard Dialog Data Validation Routines](../vs140/Standard-Dialog-Data-Validation-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)