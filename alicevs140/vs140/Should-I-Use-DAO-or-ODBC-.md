---
title: "Should I Use DAO or ODBC?"
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
ms.assetid: 9f67613f-0056-4ece-8c3a-9872e9563d57
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Should I Use DAO or ODBC?
> [!NOTE]
>  As of Visual C++ .NET, the Visual C++ environment and wizards no longer support DAO (although the DAO classes are included and you can still use them). Microsoft recommends that you use OLE DB Templates or ODBC for new projects. You should only use DAO in maintaining existing applications.  
  
 Which set of MFC classes should you use? This depends on your needs:  
  
-   Use the ODBC classes if you are working strictly with ODBC data sources, particularly in client/server situations, where the MFC ODBC classes provide better performance.  
  
-   Use the DAO classes if you are working primarily with Microsoft Jet (.mdb) databases or with other database formats that the Microsoft Jet database engine can read directly. For a list of these, see [What Databases Can I Access with DAO and ODBC?](../vs140/What-Data-Sources-Can-I-Access-with-DAO-and-ODBC-.md)  
  
-   Access ODBC data sources through the DAO classes when you want the speed of the Microsoft Jet database engine and the extra functionality of the DAO classes.  
  
    > [!NOTE]
    >  DAO requires additional hard disk space.  
  
 The DAO classes have the following advantages:  
  
-   Better performance in some cases, particularly when using Microsoft Jet (.mdb) databases.  
  
-   Compatibility with the ODBC classes and with Microsoft Access Basic and Microsoft Visual Basic.  
  
-   Access to validation rules.  
  
-   Ability to specify relations between tables.  
  
-   A richer data access model, with support for Data Definition Language (DDL) and Data Manipulation Language (DML). For more information, see [Database Definition and Manipulation](../vs140/Are-DDL-and-DML-Supported-.md).  
  
 The following table summarizes the key differences to help you choose.  
  
### Choosing Between MFC DAO and ODBC Classes  
  
|Can I|With DAO classes?|With ODBC classes?|  
|-----------|-----------------------|------------------------|  
|Access .MDB files|Yes|Yes|  
|Access ODBC data sources|Yes|Yes|  
|Available for 16 Bit|No|Yes|  
|Available for 32 Bit|Yes|Yes|  
|Available for 64 Bit|No|Yes|  
|Database compaction|Yes|No|  
|Database engine support|Microsoft Jet database engine|Target DBMS|  
|DDL support|Yes|Only through direct ODBC calls|  
|DML support|Yes|Yes|  
|Nature of the MFC implementation|"Wrapper" of DAO core functions|Simplified abstraction rather than a "wrapper" of the ODBC API|  
|Optimal for|.mdb files (Microsoft Access)|Any DBMS for which you have a driver, especially in client/server situations|  
|Transaction support|Per solution, or for ODBC data, per database|Per database|  
  
 Keep in mind that the capabilities of ODBC drivers vary. For more information, see the ODBC *Programmer's Reference* and the Help file for your ODBC driver.  
  
## See Also  
 [Data Access Frequently Asked Questions](../vs140/Data-Access-Frequently-Asked-Questions---MFC-Data-Access-.md)