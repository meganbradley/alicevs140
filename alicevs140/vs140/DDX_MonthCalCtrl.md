---
title: "DDX_MonthCalCtrl"
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
ms.assetid: f80055a7-99d1-4b99-b13d-9aae3580bcff
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_MonthCalCtrl
The `DDX_MonthCalCtrl` function manages the transfer of date data between a month calendar control ([CMonthCalCtrl](../vs140/CMonthCalCtrl-Class.md)) in a dialog box, form view, or control view object and either a [CTime](../Topic/CTime%20Class.md) or a [COleDateTime](../vs140/COleDateTime-Class.md) data member of the dialog box, form view, or control view object.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_MonthCalCtrl(  
   CDataExchange* pDX,  
   int nIDC,  
   CTime& value   
);  
void AFXAPI DDX_MonthCalCtrl(  
   CDataExchange* pDX,  
   int nIDC,  
   COleDateTime& value   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object. The framework supplies this object to establish the context of the data exchange, including its direction. You don't need to delete this object.  
  
 `nIDC`  
 The resource ID of the month calendar control associated with the member variable.  
  
 *value*  
 A reference to a `CTime` or `COleDateTime` member variable of the dialog box, form view, or control view object with which data is exchanged.  
  
## Remarks  
  
> [!NOTE]
>  The control manages a date value only. The time fields in the time object are set to reflect the creation time of the control window, or whatever time was set in the control with a call to `CMonthCalCtrl::SetCurSel`.  
  
 When `DDX_MonthCalCtrl` is called, *value* is set to the current state of the month calendar control.  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## Requirements  
 **Header:** afxdd_.h  
  
## See Also  
 [Standard Dialog Data Exchange Routines](../vs140/Standard-Dialog-Data-Exchange-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDX_DateTimeCtrl](../vs140/DDX_DateTimeCtrl.md)   
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [CMonthCalCtrl::GetCurSel](../vs140/CMonthCalCtrl--GetCurSel.md)   
 [CMonthCalCtrl::SetCurSel](../vs140/CMonthCalCtrl--SetCurSel.md)