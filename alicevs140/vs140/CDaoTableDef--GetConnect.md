---
title: "CDaoTableDef::GetConnect"
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
ms.topic: reference
ms.assetid: 2931d3ce-e924-4d16-a08d-0295038952a3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::GetConnect
Call this member function to obtain the connection string for a data source.  
  
## Syntax  
  
```  
  
CString GetConnect( );  
  
```  
  
## Return Value  
 A `CString` object containing the path and database type for the table.  
  
## Remarks  
 For a `CDaoTableDef` object that represents an attached table, the `CString` object consists of one or two parts (a database type specifier and a path to the database).  
  
 The path as shown in the table below is the full path for the directory containing the database files and must be preceded by the identifier "DATABASE=". In some cases (as with Microsoft Jet and Microsoft Excel databases), a specific filename is included in the database path argument.  
  
 The table in [CDaoTableDef::SetConnect](../vs140/CDaoTableDef--SetConnect.md) shows possible database types and their corresponding database specifiers and paths:  
  
 For Microsoft Jet database base tables, the specifier is a empty string ("").  
  
 If a password is required but not provided, the ODBC driver displays a login dialog box the first time a table is accessed and again if the connection is closed and reopened. If an attached table has the **dbAttachSavePWD** attribute, the login prompt will not appear when the table is reopened.  
  
 For related information, see the topic "Connect Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::SetConnect](../vs140/CDaoTableDef--SetConnect.md)