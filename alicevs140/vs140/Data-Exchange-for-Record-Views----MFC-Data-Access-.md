---
title: "Data Exchange for Record Views   (MFC Data Access)"
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
ms.assetid: abc52ca7-6997-47a7-98f3-f347f52b1f72
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data Exchange for Record Views   (MFC Data Access)
When you use [Add Class](../vs140/Adding-an-MFC-ODBC-Consumer.md) to map the controls in a record view's dialog template resource to the fields of a recordset, the framework manages data exchange in both directions — from recordset to controls and from controls to recordset. Using the DDX mechanism means that you do not have to write the code to transfer data back and forth yourself.  
  
 DDX for record views works in conjunction with:  
  
-   [RFX](../vs140/Record-Field-Exchange--RFX-.md) for recordsets of class `CRecordset` (ODBC).  
  
-   DFX for recordsets of class `CDaoRecordset` (DAO).  
  
 Although they differ in implementation, at the interface level RFX and DFX are very similar data exchange mechanisms. The DAO version, DFX, is modeled closely on the earlier ODBC version, RFX. If you know how to use RFX, you know how to use DFX.  
  
 RFX and DFX move data between the current record of the data source and the field data members of a recordset object. DDX moves the data from the field data members to the controls in the form. This combination fills the form controls initially and as the user moves from record to record. It can also move updated data back to the recordset and then to the data source.  
  
 The following figure shows the relationship between DDX and RFX (or DFX) for record views.  
  
 ![Dialog&#45;data exchange and record&#45;field exchange](../vs140/media/vc37XT1.gif "vc37XT1")  
Dialog Data Exchange and Record Field Exchange  
  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md). For more information about RFX, see [Record Field Exchange (RFX)](../vs140/Record-Field-Exchange--RFX-.md).  
  
## See Also  
 [Record Views  (MFC Data Access)](../vs140/Record-Views---MFC-Data-Access-.md)   
 [ODBC Driver List](../vs140/ODBC-Driver-List.md)