---
title: "Displaying and Manipulating Data in a Form"
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
ms.assetid: c56185c4-12cb-40b1-b499-02b29ea83e3a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Displaying and Manipulating Data in a Form
Many data-access applications select data and display it in fields in a form. The database class [CRecordView](../vs140/CRecordView-Class.md) gives you a [CFormView](../vs140/CFormView-Class.md) object directly connected to a recordset object. The record view uses [dialog data exchange (DDX)](../vs140/Dialog-Data-Exchange-and-Validation.md) to move the values of the fields of the current record from the recordset to the controls on the form and to move updated information back to the recordset. The recordset, in turn, uses record field exchange (RFX) to move data between its field data members and the corresponding columns in a table on the data source.  
  
 You can use the MFC Application Wizard or **Add Class** (as described in [Adding an MFC ODBC Consumer](../vs140/Adding-an-MFC-ODBC-Consumer.md)) to create the view class and its associated recordset class in conjunction.  
  
 The record view and its recordset are destroyed when you close the document. For more information about record views, see [Record Views](../vs140/Record-Views---MFC-Data-Access-.md). For more information about RFX, see [Record Field Exchange (RFX)](../vs140/Record-Field-Exchange--RFX-.md).  
  
## See Also  
 [ODBC and MFC](../vs140/ODBC-and-MFC.md)