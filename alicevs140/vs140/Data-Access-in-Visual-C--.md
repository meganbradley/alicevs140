---
title: "Data Access in Visual C++"
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
ms.assetid: a9455752-39c4-4457-b14e-197772d3df0b
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data Access in Visual C++
Since 2011 Microsoft [has aligned on ODBC](http://blogs.technet.com/b/dataplatforminsider/archive/2011/08/29/microsoft-aligning-with-odbc.aspx) as the standard for native applications to connecting to SQL Server databases. For more information, see the [FAQ](http://social.msdn.microsoft.com/Forums/sqlserver/e696d0ac-f8e2-4b19-8a08-7a357d3d780f/microsoft-is-aligning-with-odbc-for-native-relational-data-access-faq?forum=sqldataaccess). For modern native C++ applications running on Windows, the preferred way to connect to SQL databases, including [SQL Database](http://azure.microsoft.com/services/sql-database/) instances hosted in Azure, is to use the [ODBC Driver 11 for SQL Server on Windows](http://msdn.microsoft.com/library/jj730314.aspx).  
  
 For low-overhead local database instances, you can use [SQL Server 2014 Express LocalDB](http://msdn.microsoft.com/library/hh510202.aspx) which does not require an instance of SQL to be running. C++/CLI libraries can use either the native ODBC drivers or ADO.NET as well as Azure data services for .NET. For more information, see [Data Access Using ADO.NET in C++](../vs140/Data-Access-Using-ADO.NET--C---CLI-.md) and [Accessing Data (Visual Studio)](assetId:///9812a6d5-23d2-4427-8b98-70a2abfec3bc).  
  
## In This Section  
 This section covers legacy database programming technologies. These pages are not always relevant for new applications.  
  
 [Data Access Programming](../vs140/Data-Access-Programming--MFC-ATL-.md)  
 Describes legacy data access programming with Visual C++, where the preferred way is to use one of the class libraries such as the Active Template Class Library (ATL) or Microsoft Foundation Class (MFC) Library, which simplify working with the database APIs.  
  
 [OLE DB Programming](../vs140/OLE-DB-Programming.md)  
 Provides links to conceptual topics discussing OLE DB database technology and the OLE DB Template Library.  
  
 [Open Database Connectivity (ODBC) via MFC](../vs140/Open-Database-Connectivity--ODBC-.md)  
 Provides links to conceptual topics discussing targeting ODBC with MFC.  
  
 [Data-Bound Controls (ADO and RDO)](../vs140/Data-Bound-Controls--ADO-and-RDO-.md)  
 Discusses a reusable databinding mechanism through ActiveX controls in MFC projects that lets you rapidly develop database applications.  
  
## Related Sections  
 [OLE DB Templates](../vs140/OLE-DB-Templates.md)  
 Provides reference material for the OLE DB consumer and provider templates, a set of template classes that implement many commonly used OLE DB interfaces.  
  
 [MFC Reference](../vs140/MFC-Desktop-Applications.md)  
 Provides reference material for the MFC Library, a set of classes that constitute an application framework, which is the framework of an application written for the Windows API.  
  
## See Also  
 [Data Access Technologies Road Map](http://msdn.microsoft.com/library/ms810810.aspx#mdac%20technologies%20road%20map%20old_topic9)