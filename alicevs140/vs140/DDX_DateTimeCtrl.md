---
title: "DDX_DateTimeCtrl"
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
ms.assetid: 27885693-12b5-48ef-bb9d-be3d56d5747d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_DateTimeCtrl
The `DDX_DateTimeCtrl` function manages the transfer of date and/or time data between a date and time picker control ([CDateTimeCtrl](../vs140/CDateTimeCtrl-Class.md)) in a dialog box or form view object and either a [CTime](../Topic/CTime%20Class.md) or a [COleDateTime](../vs140/COleDateTime-Class.md) data member of the dialog box or form view object.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_DateTimeCtrl(  
   CDataExchange* pDX,  
   int nIDC,  
   CTime& value   
);  
void AFXAPI DDX_DateTimeCtrl(  
   CDataExchange* pDX,  
   int nIDC,  
   COleDateTime& value   
);  
void AFXAPI DDX_DateTimeCtrl(  
   CDataExchange* pDX,  
   int nIDC,  
   CString& value   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object. The framework supplies this object to establish the context of the data exchange, including its direction. You don't need to delete this object.  
  
 `nIDC`  
 The resource ID of the date and time picker control associated with the member variable.  
  
 *value*  
 In the first two versions, a reference to a `CTime` or `COleDateTime` member variable, dialog box, form view, or control view object with which data is exchanged. In the third version, a reference to a `CString` data member control view object.  
  
## Remarks  
 When `DDX_DateTimeCtrl` is called, *value* is set to the current state of the date and time picker control, or the control is set to *value*, depending on the direction of the exchange.  
  
 In the third version above, `DDX_DateTimeCtrl` manages the transfer of `CString` data between a date time control and a [CString](../vs140/CStringT-Class.md) data member of the control view object. The string is formatted using the current locale's rules for formatting dates and times.  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## Requirements  
 **Header:** afxoledb.h  
  
## See Also  
 [Standard Dialog Data Exchange Routines](../vs140/Standard-Dialog-Data-Exchange-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [CDateTimeCtrl::SetRange](../vs140/CDateTimeCtrl--SetRange.md)   
 [CDateTimeCtrl::GetRange](../vs140/CDateTimeCtrl--GetRange.md)   
 [DDV_MinMaxDateTime](../vs140/DDV_MinMaxDateTime.md)