---
title: "Data Access Programming (MFC-ATL)"
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
H1: Data Access Programming (MFC/ATL)
ms.assetid: def97b2c-b5a6-445f-afeb-308050fd4852
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data Access Programming (MFC-ATL)
Visual C++ provides several ways to work with databases. The preferred way is to use one of the class libraries such as the Active Template Class Library (ATL) or Microsoft Foundation Class (MFC) Library, which simplify working with the database APIs.  
  
> [!NOTE]
>  This topic covers the older technologies you can use for database programming in Visual C++. For information on data access programming using Visual C++ and SQL Server, see [Data Access Using ADO.NET in C++/CLI](../vs140/Data-Access-Using-ADO.NET--C---CLI-.md), and [Accessing Data (Visual Studio)](assetId:///9812a6d5-23d2-4427-8b98-70a2abfec3bc).  
  
 The library classes support the following kinds of data access:  
  
-   ATL provides OLE DB templates and database attributes.  
  
-   MFC provides Open Database Connectivity (ODBC) and an ODBC driver.  
  
 These libraries supply abstractions that simplify working with databases, complete with the speed, power, and flexibility of C++. They integrate your data access work with the library's application framework.  
  
 Alternately, you can directly call database API functions from the COM, ODBC, or DAO software development kits (SDKs). For information about programming directly with the COM, DAO, or ODBC API functions, see the COM SDK, DAO SDK, or ODBC SDK.  
  
 Use ATL OLE DB if you need to access data, regardless of the form in which it is stored. Use the MFC ODBC classes when you are not using Microsoft Jet (.mdb) databases and want to work with the ODBC API for complete data-source independence. Use the MFC DAO classes when you want to work with Microsoft Jet (.mdb) databases or with external databases such as ODBC data sources.  
  
> [!NOTE]
>  Microsoft recommends using OLE DB or ODBC for new projects. DAO should only be used in maintaining existing applications.  
  
 Besides writing stand-alone database applications, you can often use a database effectively in other kinds of programs as a convenient storage and retrieval medium.  
  
|To learn more about|See|  
|-------------------------|---------|  
|**Selecting a database technology**||  
|ODBC vs. DAO|[Should I Use DAO or ODBC?](../vs140/Should-I-Use-DAO-or-ODBC-.md)|  
|Using the Microsoft Knowledge Base to find additional articles on database topics written by product support engineers|[Microsoft Knowledge Base](../vs140/Where-Can-I-Find-Microsoft-Knowledge-Base-Articles-on-Database-Topics-.md)|  
|**ATL Database Support (OLE DB)**||  
|OLE DB programming (conceptual topics)|[OLE DB Programming Overview](../vs140/OLE-DB-Programming-Overview.md)|  
|Using the OLE DB consumer templates (conceptual topics)|[OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)|  
|OLE DB consumer attributes|[OLE DB Consumer Attributes](../vs140/OLE-DB-Consumer-Attributes.md)|  
|Using the OLE DB provider templates (conceptual topics)|[OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)|  
|Adding an OLE DB consumer to an MFC project|[Creating an OLE DB Consumer](../vs140/Creating-an-OLE-DB-Consumer.md)|  
|**MFC Database Support (ODBC and DAO)**||  
|What DAO and ODBC are|[What Are DAO and ODBC?](../vs140/What-Are-DAO-and-ODBC-.md)|  
|When to use the MFC database classes|[When Should I Use the Database Classes?](../vs140/When-Should-I-Use-the-Database-Classes-.md)|  
|Learn about the MFC database programming model|[What Is the MFC Database Programming Model?](../vs140/What-Is-the-MFC-Database-Programming-Model-.md).|  
|Choose between the MFC DAO classes and the MFC ODBC classes|[Should I Use DAO or ODBC?](../vs140/Should-I-Use-DAO-or-ODBC-.md).|  
|Data sources you can access with DAO and ODBC|[What Data Sources Can I Access with DAO and ODBC?](../vs140/What-Data-Sources-Can-I-Access-with-DAO-and-ODBC-.md)|  
|Open Database Connectivity (ODBC)|[ODBC and MFC](../vs140/ODBC-and-MFC.md)|  
|Whether you can call DAO or ODBC APIs directly while using the classes|[Can I Call DAO or ODBC Directly?](../vs140/Can-I-Call-DAO-or-ODBC-Directly-.md)|  
|What ODBC drivers are provided|[ODBC Driver List](../vs140/ODBC-Driver-List.md)|  
|How the database classes work with the MFC document/view architecture|[MFC: Using Database Classes with Documents and Views](../vs140/MFC--Using-Database-Classes-with-Documents-and-Views.md)|  
|Installing MFC database support; what ODBC drivers are installed in Visual C++ by default; what ODBC and DAO SDK components are installed|[Installing MFC Database Support](../vs140/Installing-MFC-Database-Support.md)|  
|**Data-Bound Controls (ADO and RDO)**||  
|Writing a program that uses data-bound controls|[Data-Bound Controls (ADO and RDO)](../vs140/Data-Bound-Controls--ADO-and-RDO-.md)|  
|Data binding using ActiveX controls|[MFC ActiveX Controls: Using Data Binding in an ActiveX Control](../vs140/MFC-ActiveX-Controls--Using-Data-Binding-in-an-ActiveX-Control.md)|  
|Distributing ActiveX controls|[MFC ActiveX Controls: Distributing ActiveX Controls](../vs140/MFC-ActiveX-Controls--Distributing-ActiveX-Controls.md)|  
  
## See Also  
 [Data Access](../vs140/Data-Access-in-Visual-C--.md)