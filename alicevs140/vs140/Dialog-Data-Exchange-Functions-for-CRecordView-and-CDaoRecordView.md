---
title: "Dialog Data Exchange Functions for CRecordView and CDaoRecordView"
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
ms.assetid: 0d8cde38-3a2c-4100-9589-ac80a7b1ce91
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Dialog Data Exchange Functions for CRecordView and CDaoRecordView
This topic lists the DDX_Field functions used to exchange data between a [CRecordset](../vs140/CRecordset-Class.md) and a [CRecordView](../vs140/CRecordView-Class.md) form or a [CDaoRecordset](../vs140/CDaoRecordset-Class.md) and a [CDaoRecordView](../vs140/CDaoRecordView-Class.md) form.  
  
> [!NOTE]
>  DDX_Field functions are like DDX functions in that they exchange data with controls in a form. But unlike DDX, they exchange data with the fields of the view's associated recordset object rather than with fields of the record view itself. For more information, see classes `CRecordView` and `CDaoRecordView`.  
  
### DDX_Field Functions  
  
|||  
|-|-|  
|[DDX_FieldCBIndex](../vs140/DDX_FieldCBIndex.md)|Transfers integer data between a recordset field data member and the index of the current selection in a combo box in a [CRecordView](../vs140/CRecordView-Class.md) or [CDaoRecordView](../vs140/CDaoRecordView-Class.md).|  
|[DDX_FieldCBString](../vs140/DDX_FieldCBString.md)|Transfers `CString` data between a recordset field data member and the edit control of a combo box in a `CRecordView` or `CDaoRecordView`. When moving data from the recordset to the control, this function selects the item in the combo box that begins with the characters in the specified string.|  
|[DDX_FieldCBStringExact](../vs140/DDX_FieldCBStringExact.md)|Transfers `CString` data between a recordset field data member and the edit control of a combo box in a `CRecordView` or `CDaoRecordView`. When moving data from the recordset to the control, this function selects the item in the combo box that exactly matches the specified string.|  
|[DDX_FieldCheck](../vs140/DDX_FieldCheck.md)|Transfers Boolean data between a recordset field data member and a check box in a `CRecordView` or `CDaoRecordView`.|  
|[DDX_FieldLBIndex](../vs140/DDX_FieldLBIndex.md)|Transfers integer data between a recordset field data member and the index of the current selection in a list box in a `CRecordView` or `CDaoRecordView`.|  
|[DDX_FieldLBString](../vs140/DDX_FieldLBString.md)|Manages the transfer of [CString](../vs140/CStringT-Class.md) data between a list-box control and the field data members of a recordset. When moving data from the recordset to the control, this function selects the item in the list box that begins with the characters in the specified string.|  
|[DDX_FieldLBStringExact](../vs140/DDX_FieldLBStringExact.md)|Manages the transfer of `CString` data between a list-box control and the field data members of a recordset. When moving data from the recordset to the control, this function selects the first item that exactly matches the specified string.|  
|[DDX_FieldRadio](../vs140/DDX_FieldRadio.md)|Transfers integer data between a recordset field data member and a group of radio buttons in a `CRecordView` or `CDaoRecordView`.|  
|[DDX_FieldScroll](../vs140/DDX_FieldScroll.md)|Sets or gets the scroll position of a scroll bar control in a `CRecordView` or `CDaoRecordView`. Call from your [DoFieldExchange](../vs140/CDaoRecordset--DoFieldExchange.md) function.|  
|[DDX_FieldText](../vs140/DDX_FieldText.md)|Overloaded versions are available for transferring `int`, **UINT**, **long**, `DWORD`, [CString](../vs140/CStringT-Class.md), **float**, **double**, **short**, [COleDateTime](../vs140/COleDateTime-Class.md), and [COleCurrency](../vs140/COleCurrency-Class.md) data between a recordset field data member and an edit box in a `CRecordView` or `CDaoRecordView`.|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)