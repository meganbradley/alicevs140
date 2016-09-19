---
title: "Redistributing ODBC Components to Your Customers"
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
ms.assetid: 17b065b4-a307-4b89-99ac-d05831cfab87
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Redistributing ODBC Components to Your Customers
If you incorporate the functionality of the ODBC Administrator programs into your application, you must also distribute to your users the files that run these programs. These ODBC files reside in the \OS\System directory of the Visual C++ CD-ROM. The Redistrb.wri file and the license agreement in the same directory contain a list of ODBC files that you can redistribute.  
  
 Consult the documentation for any ODBC drivers you plan to ship. You need to determine which DLLs and other files to ship.  
  
 You should also read [Installing Database Support](../vs140/Installing-Database-Support--MFC-ATL-.md) for information about ODBC components and drivers and read [Redistributing Controls](../vs140/Redistributing-Controls.md), which explains how to redistribute ActiveX controls.  
  
 In addition, you need to include one other file in most cases. The Odbccr32.dll is the ODBC Cursor Library. This library gives Level 1 drivers the capability of forward and backward scrolling. It also provides the capability of supporting snapshots. For more information about the ODBC Cursor Library, see [ODBC: The ODBC Cursor Library](../vs140/ODBC--The-ODBC-Cursor-Library.md).  
  
 The following topics provide more information about using ODBC with the database classes:  
  
-   [ODBC: The ODBC Cursor Library](../vs140/ODBC--The-ODBC-Cursor-Library.md)  
  
-   [ODBC: Configuring an ODBC Data Source](../vs140/ODBC--Configuring-an-ODBC-Data-Source.md)  
  
-   [ODBC: Calling ODBC API Functions Directly](../vs140/ODBC--Calling-ODBC-API-Functions-Directly.md)  
  
## See Also  
 [ODBC Basics](../vs140/ODBC-Basics.md)   
 [ODBC Administrator](../vs140/ODBC-Administrator.md)