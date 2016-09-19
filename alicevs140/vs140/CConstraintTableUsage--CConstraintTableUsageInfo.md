---
title: "CConstraintTableUsage, CConstraintTableUsageInfo"
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
ms.assetid: 666b44de-3922-4c5e-ad17-d5ea27120174
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CConstraintTableUsage, CConstraintTableUsageInfo
Call the typedef class **CConstraintTableUsage** to implement its parameter class **CConstraintTableUsageInfo**.  
  
## Remarks  
 See [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md) for more information on using typedef classes.  
  
 This class identifies the tables used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.  
  
 The following table lists the class data members and their corresponding OLE DB Columns. See [CONSTRAINT_TABLE_USAGE Rowset](https://msdn.microsoft.com/en-us/library/ms724522.aspx) in the *OLE DB Programmer's Reference* for more information about the schema and columns.  
  
|Data members|OLE DB columns|  
|------------------|--------------------|  
|m_szTableCatalog|TABLE_CATALOG|  
|m_szTableSchema|TABLE_SCHEMA|  
|m_szTableName|TABLE_NAME|  
|m_szConstraintCatalog|CONSTRAINT_CATALOG|  
|m_szConstraintSchema|CONSTRAINT_SCHEMA|  
|m_szConstraintName|CONSTRAINT_NAME|  
  
## Requirements  
 **Header:** atldbsch.h  
  
## See Also  
 [CRestrictions Class](../vs140/CRestrictions-Class.md)