---
title: "CForeignKeys, CForeignKeysInfo"
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
ms.assetid: 1c401a4a-0827-4255-9214-bc893e1cd79d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CForeignKeys, CForeignKeysInfo
Call the typedef class **CForeignKeys** to implement its parameter class **CForeignKeysInfo**.  
  
## Remarks  
 See [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md) for more information on using typedef classes.  
  
 This class identifies the foreign key columns defined in the catalog by a given user.  
  
 The following table lists the class data members and their corresponding OLE DB Columns. See [FOREIGN_KEYS Rowset](https://msdn.microsoft.com/en-us/library/ms711276.aspx) in the *OLE DB Programmer's Reference* for more information about the schema and columns.  
  
|Data members|OLE DB columns|  
|------------------|--------------------|  
|m_szPKTableCatalog|PK_TABLE_CATALOG|  
|m_szPKTableSchema|PK_TABLE_SCHEMA|  
|m_szPKTableName|PK_TABLE_NAME|  
|m_szPKColumnName|PK_COLUMN_NAME|  
|m_guidPKColumn|PK_COLUMN_GUID|  
|m_nPKColumnPropID|PK_COLUMN_PROPID|  
|m_szFKTableCatalog|FK_TABLE_CATALOG|  
|m_szFKTableSchema|FK_TABLE_SCHEMA|  
|m_szFKTableName|FK_TABLE_NAME|  
|m_szFKColumnName|FK_COLUMN_NAME|  
|m_guidFKColumn|FK_COLUMN_GUID|  
|m_nFKColumnPropID|FK_COLUMN_PROPID|  
|m_nOrdinal|ORDINAL|  
|m_szUpdateRule|UPDATE_RULE|  
|m_szDeleteRule|DELETE_RULE|  
  
## Requirements  
 **Header:** atldbsch.h  
  
## See Also  
 [CRestrictions Class](../vs140/CRestrictions-Class.md)