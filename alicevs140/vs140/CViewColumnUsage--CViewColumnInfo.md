---
title: "CViewColumnUsage, CViewColumnInfo"
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
ms.assetid: 4af14d6b-b224-4d72-b035-9d3aaacde32f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CViewColumnUsage, CViewColumnInfo
Call the typedef class **CViewColumnUsage** to implement its parameter class **CViewColumnInfo**.  
  
## Remarks  
 See [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md) for more information on using typedef classes.  
  
 This class identifies the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.  
  
 The following table lists the class data members and their corresponding OLE DB Columns. See [VIEW_COLUMN_USAGE Rowset](https://msdn.microsoft.com/en-us/library/ms714896.aspx) in the *OLE DB Programmer's Reference* for more information about the schema and columns.  
  
|Data members|OLE DB columns|  
|------------------|--------------------|  
|m_szCatalog|VIEW_CATALOG|  
|m_szSchema|VIEW_SCHEMA|  
|m_szName|VIEW_NAME|  
|m_szTableCatalog|TABLE_CATALOG|  
|m_szTableSchema|TABLE_SCHEMA|  
|m_szTableName|TABLE_NAME|  
|m_szColumnName|COLUMN_NAME|  
|m_guidColumn|COLUMN_GUID|  
|m_nColumnPropID|COLUMN_PROPID|  
  
## Requirements  
 **Header:** atldbsch.h  
  
## See Also  
 [CRestrictions Class](../vs140/CRestrictions-Class.md)