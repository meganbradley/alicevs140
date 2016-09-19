---
title: "DDX_FieldCBStringExact"
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
ms.assetid: 3fc9327b-5439-44dd-80cb-e119d62a422e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_FieldCBStringExact
The `DDX_FieldCBStringExact` function manages the transfer of [CString](../vs140/CStringT-Class.md) data between the edit control of a combo box control in a record view and a `CString` field data member of a recordset associated with the record view.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_FieldCBStringExact(  
   CDataExchange* pDX,  
   int nIDC,  
   CString& value,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldCBStringExact(  
   CDataExchange* pDX,  
   int nIDC,  
   CString& value,  
   CDaoRecordset* pRecordset   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of a control in the [CRecordView](../vs140/CRecordView-Class.md) or [CDaoRecordView](../vs140/CDaoRecordView-Class.md) object.  
  
 *value*  
 A reference to a field data member in the associated `CRecordset` or `CDaoRecordset` object.  
  
 `pRecordset`  
 A pointer to the [CRecordset](../vs140/CRecordset-Class.md) or [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object with which data is exchanged.  
  
## Remarks  
 When moving data from the recordset to the control, this function sets the current selection in the combo box to the first row that exactly matches the string specified in *value*. On a transfer from the recordset to the control, if the recordset field is NULL, any selection is removed from the combo box and the edit box of the combo box is set to empty. On a transfer from control to recordset, if the control is empty, the recordset field is set to NULL.  
  
 Use the first version if you are working with the ODBC-based classes. Use the second version if you are working with the DAO-based classes.  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md). For examples and more information about DDX for [CRecordView](../vs140/CRecordView-Class.md) and [CDaoRecordView](../vs140/CDaoRecordView-Class.md) fields, see the article [Record Views](../vs140/Record-Views---MFC-Data-Access-.md).  
  
## Example  
 See [DDX_FieldText](../vs140/DDX_FieldText.md) for a general DDX_Field example. Calls to `DDX_FieldCBStringExact` would be similar.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDX_FieldText](../vs140/DDX_FieldText.md)   
 [DDX_FieldRadio](../vs140/DDX_FieldRadio.md)   
 [DDX_FieldLBString](../vs140/DDX_FieldLBString.md)   
 [DDX_FieldLBStringExact](../vs140/DDX_FieldLBStringExact.md)   
 [DDX_FieldCBString](../vs140/DDX_FieldCBString.md)