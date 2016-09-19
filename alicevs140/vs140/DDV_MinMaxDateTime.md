---
title: "DDV_MinMaxDateTime"
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
ms.assetid: ec52b675-5267-4bbd-9d19-71b339681ed3
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDV_MinMaxDateTime
Call `DDV_MinMaxDateTime` to verify that the time/date value in the date and time picker control ([CDateTimeCtrl](../vs140/CDateTimeCtrl-Class.md)) associated with *refValue* falls between `refMinRange` and `refMaxRange`.  
  
## Syntax  
  
```  
  
      void AFXAPI DDV_MinMaxDateTime(  
   CDataExchange* pDX,  
   CTime& refValue,  
   const CTime* refMinRange,  
   const CTime* refMaxRange   
);  
void AFXAPI DDV_MinMaxDateTime(  
   CDataExchange* pDX,  
   COleDateTime& refValue,  
   const COleDateTime* refMinRange,  
   const COleDateTime* refMaxRange   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object. The framework supplies this object to establish the context of the data exchange, including its direction. You don't need to delete this object.  
  
 *refValue*  
 A reference to a [CTime](../Topic/CTime%20Class.md) or [COleDateTime](../vs140/COleDateTime-Class.md) object associated with a member variable of the dialog box, form view, or control view object. This object contains the data to be validated.  
  
 `refMinRange`  
 Minimum date/time value allowed.  
  
 `refMaxRange`  
 Maximum date/time value allowed.  
  
## Remarks  
 For more information about DDV, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## Requirements  
 **Header:** afxdd_.h  
  
## See Also  
 [Standard Dialog Data Validation Routines](../vs140/Standard-Dialog-Data-Validation-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDX_DateTimeCtrl](../vs140/DDX_DateTimeCtrl.md)   
 [DDV_MinMaxMonth](../vs140/DDV_MinMaxMonth.md)