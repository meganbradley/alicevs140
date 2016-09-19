---
title: "DDX_FieldText"
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
ms.assetid: 03c5a8ec-1223-4849-b27b-d4e66a50d69d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_FieldText
The `DDX_FieldText` function manages the transfer of `int`, **short**, **long**, `DWORD`, [CString](../vs140/CStringT-Class.md), **float**, **double**, **BOOL**, or **BYTE** data between an edit box control and the field data members of a recordset.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   BYTE& value,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   int& value,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   UINT& value,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   long& value,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   DWORD& value,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   CString& value,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   float& value,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   double& value,  
   CRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   short& value,  
   CDaoRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   BOOL& value,  
   CDaoRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   BYTE& value,  
   CDaoRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   long& value,  
   CDaoRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   DWORD& value,  
   CDaoRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   CString& value,  
   CDaoRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   float& value,  
   CDaoRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   double& value,  
   CDaoRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   COleDateTime& value,  
   CDaoRecordset* pRecordset   
);  
void AFXAPI DDX_FieldText(  
   CDataExchange* pDX,  
   int nIDC,  
   COleCurrency& value,  
   CDaoRecordset* pRecordset   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of a control in the [CRecordView](../vs140/CRecordView-Class.md) or [CDaoRecordView](../vs140/CDaoRecordView-Class.md) object.  
  
 *value*  
 A reference to a field data member in the associated `CRecordset` or `CDaoRecordset` object. The data type of value depends on which of the overloaded versions of `DDX_FieldText` you use.  
  
 `pRecordset`  
 A pointer to the [CRecordset](../vs140/CRecordset-Class.md) or [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object with which data is exchanged. This pointer enables `DDX_FieldText` to detect and set Null values.  
  
## Remarks  
 For [CDaoRecordset](../vs140/CDaoRecordset-Class.md) objects, `DDX_FieldText` also manages transferring [COleDateTime](../vs140/COleDateTime-Class.md), and [COleCurrency](../vs140/COleCurrency-Class.md) values. An empty edit box control indicates a Null value. On a transfer from the recordset to the control, if the recordset field is Null, the edit box is set to empty. On a transfer from control to recordset, if the control is empty, the recordset field is set to Null.  
  
 Use the versions with [CRecordset](../vs140/CRecordset-Class.md) parameters if you are working with the ODBC-based classes. Use the versions with [CDaoRecordset](../vs140/CDaoRecordset-Class.md) parameters if you are working with the DAO-based classes.  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md). For examples and more information about DDX for [CRecordView](../vs140/CRecordView-Class.md) and [CDaoRecordView](../vs140/CDaoRecordView-Class.md) fields, see the article [Record Views](../vs140/Record-Views---MFC-Data-Access-.md).  
  
## Example  
 The following `DoDataExchange` function for a [CRecordView](../vs140/CRecordView-Class.md) contains `DDX_FieldText` function calls for three data types: `IDC_COURSELIST` is a combo box; the other two controls are edit boxes. For DAO programming, the *m_pSet* parameter is a pointer to a [CRecordset](../vs140/CRecordset-Class.md) or [CDaoRecordset](../vs140/CDaoRecordset-Class.md).  
  
 [!CODE [NVC_MFCDatabase#43](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#43)]  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDX_FieldRadio](../vs140/DDX_FieldRadio.md)   
 [DDX_FieldLBString](../vs140/DDX_FieldLBString.md)   
 [DDX_FieldLBStringExact](../vs140/DDX_FieldLBStringExact.md)   
 [DDX_FieldCBString](../vs140/DDX_FieldCBString.md)   
 [DDX_FieldCBStringExact](../vs140/DDX_FieldCBStringExact.md)   
 [DDX_FieldCBIndex](../vs140/DDX_FieldCBIndex.md)   
 [DDX_FieldLBIndex](../vs140/DDX_FieldLBIndex.md)   
 [DDX_FieldScroll](../vs140/DDX_FieldScroll.md)