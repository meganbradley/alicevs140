---
title: "DDX_FieldLBIndex"
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
ms.assetid: b424516a-f7c7-45ce-9a74-4e55a181f5a3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_FieldLBIndex
The `DDX_FieldLBIndex` function synchronizes the index of the selected item in a list box control in a record view and an `int` field data member of a recordset associated with the record view.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_FieldLBIndex(  
   CDataExchange* pDX,  
   int nIDC,  
   int& index,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldLBIndex(  
   CDataExchange* pDX,  
   int nIDC,  
   int& index,  
   CDaoRecordset* pRecordset   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of a control in the [CRecordView](../vs140/CRecordView-Class.md) or [CDaoRecordView](../vs140/CDaoRecordView-Class.md) object.  
  
 *index*  
 A reference to a field data member in the associated `CRecordset` or `CDaoRecordset` object.  
  
 `pRecordset`  
 A pointer to the [CRecordset](../vs140/CRecordset-Class.md) or [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object with which data is exchanged.  
  
## Remarks  
 When moving data from the recordset to the control, this function sets the selection in the control based on the value specified in *index*. On a transfer from the recordset to the control, if the recordset field is Null, MFC sets the value of the index to 0. On a transfer from control to recordset, if the control is empty, the recordset field is set to 0.  
  
 Use the first version if you are working with the ODBC-based classes. Use the second version if you are working with the DAO-based classes.  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md). For examples and more information about DDX for [CRecordView](../vs140/CRecordView-Class.md) and [CDaoRecordView](../vs140/CDaoRecordView-Class.md) fields, see the article [Record Views](../vs140/Record-Views---MFC-Data-Access-.md).  
  
## Example  
 See [DDX_FieldText](../vs140/DDX_FieldText.md) for a general DDX_Field example.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDX_FieldText](../vs140/DDX_FieldText.md)   
 [DDX_FieldRadio](../vs140/DDX_FieldRadio.md)   
 [DDX_FieldLBString](../vs140/DDX_FieldLBString.md)   
 [DDX_FieldLBStringExact](../vs140/DDX_FieldLBStringExact.md)   
 [DDX_FieldCBStringExact](../vs140/DDX_FieldCBStringExact.md)   
 [DDX_FieldCBIndex](../vs140/DDX_FieldCBIndex.md)   
 [DDX_FieldScroll](../vs140/DDX_FieldScroll.md)   
 [DDX_LBIndex](../vs140/DDX_LBIndex.md)