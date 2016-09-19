---
title: "Record Views  (MFC Data Access)"
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
ms.assetid: 562122d9-01d8-4284-acf6-ea109ab0408d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Record Views  (MFC Data Access)
This section applies only to the MFC ODBC and DAO classes. For information about OLE DB record views, see [COleDBRecordView](../vs140/COleDBRecordView-Class.md) and [Using OLE DB Record Views](../vs140/Using-OLE-DB-Record-Views.md).  
  
 To support form-based data-access applications, the class library provides class [CRecordView](../vs140/CRecordView-Class.md) and class [CDaoRecordView](../vs140/CDaoRecordView-Class.md). A record view is a form view object whose controls are mapped directly to the field data members of a [recordset](../vs140/Recordset--ODBC-.md) object (and indirectly to the corresponding columns in a query result or table on the data source). Like their base class [CFormView](../vs140/CFormView-Class.md), `CRecordView` and `CDaoRecordView` are based on a dialog template resource.  
  
## Form Uses  
 Forms are useful for a variety of data-access tasks:  
  
-   Entering data  
  
-   Performing read-only examination of data  
  
-   Updating data  
  
## Further Reading About Record Views  
 The material in topics applies to both the ODBC-based and the DAO-based classes. Use `CRecordView` for ODBC and `CDaoRecordView` for DAO.  
  
 Topics include:  
  
-   [Features of Record View Classes](../vs140/Features-of-Record-View-Classes---MFC-Data-Access-.md)  
  
-   [Data Exchange for Record Views](../vs140/Data-Exchange-for-Record-Views----MFC-Data-Access-.md)  
  
-   [Your Role in Working with a Record View](../vs140/Your-Role-in-Working-with-a-Record-View---MFC-Data-Access-.md)  
  
-   [Designing and Creating a Record View](../vs140/Designing-and-Creating-a-Record-View---MFC-Data-Access-.md)  
  
-   [Using a Record View](../vs140/Using-a-Record-View---MFC-Data-Access-.md)  
  
## See Also  
 [Data Access Programming (MFC/ATL)](../vs140/Data-Access-Programming--MFC-ATL-.md)   
 [ODBC Driver List](../vs140/ODBC-Driver-List.md)