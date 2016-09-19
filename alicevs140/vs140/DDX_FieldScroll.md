---
title: "DDX_FieldScroll"
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
ms.assetid: 929184e9-d8ac-434d-bc2e-73dbfca2f085
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_FieldScroll
The `DDX_FieldScroll` function synchronizes the scroll position of a scroll bar control in a record view and an `int` field data member of a recordset associated with the record view (or with whatever integer variable you choose to map it to).  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_FieldScroll(  
   CDataExchange* pDX,  
   int nIDC,  
   int& value,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldScroll(  
   CDataExchange* pDX,  
   int nIDC,  
   int& value,  
   CDaoRecordset* pRecordset   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 *nIDC\**  
 The ID of the first in a group (with style **WS_GROUP**) of adjacent radio button controls in the [CRecordView](../vs140/CRecordView-Class.md) or [CDaoRecordView](../vs140/CDaoRecordView-Class.md) object.  
  
 *value*  
 A reference to a field data member in the associated `CRecordset` or `CDaoRecordset` object.  
  
 `pRecordset`  
 A pointer to the [CRecordset](../vs140/CRecordset-Class.md) or [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object with which data is exchanged.  
  
## Remarks  
 When moving data from the recordset to the control, this function sets the scroll position of the scroll bar control to the value specified in *value*. On a transfer from the recordset to the control, if the recordset field is Null, the scroll bar control is set to 0. On a transfer from control to recordset, if the control is empty, the value of the recordset field is 0.  
  
 Use the first version if you are working with the ODBC-based classes. Use the second version if you are working with the DAO-based classes.  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md). For examples and more information about DDX for [CRecordView](../vs140/CRecordView-Class.md) and [CDaoRecordView](../vs140/CDaoRecordView-Class.md) fields, see the article [Record Views](../vs140/Record-Views---MFC-Data-Access-.md).  
  
## Example  
 See [DDX_FieldText](../vs140/DDX_FieldText.md) for a general DDX_Field example. Calls to `DDX_FieldScroll` would be similar.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDX_FieldText](../vs140/DDX_FieldText.md)   
 [DDX_FieldLBString](../vs140/DDX_FieldLBString.md)   
 [DDX_FieldLBStringExact](../vs140/DDX_FieldLBStringExact.md)   
 [DDX_FieldCBString](../vs140/DDX_FieldCBString.md)   
 [DDX_FieldCBStringExact](../vs140/DDX_FieldCBStringExact.md)   
 [DDX_FieldCBIndex](../vs140/DDX_FieldCBIndex.md)   
 [DDX_FieldLBIndex](../vs140/DDX_FieldLBIndex.md)   
 [DDX_Scroll](../vs140/DDX_Scroll.md)