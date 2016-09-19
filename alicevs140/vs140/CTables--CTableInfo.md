---
title: "CTables, CTableInfo"
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
ms.assetid: 57670f1b-ba99-43b0-b406-4c75b44f14f6
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTables, CTableInfo
Call the typedef class **CTables** to implement its parameter class **CTableInfo**.  
  
## Remarks  
 See [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md) for more information on using typedef classes.  
  
 This class identifies the privileges on tables, defined in the catalog, that are available to or granted by a given user.  
  
 The following table lists the class data members and their corresponding OLE DB Columns. See [TABLES Rowset](https://msdn.microsoft.com/en-us/library/ms716980.aspx) in the *OLE DB Programmer's Reference* for more information about the schema and columns.  
  
|Data members|OLE DB columns|  
|------------------|--------------------|  
|m_szCatalog|TABLE_CATALOG|  
|m_szSchema|TABLE_SCHEMA|  
|m_szName|TABLE_NAME|  
|m_szType|TABLE_TYPE|  
|m_guidTable|TABLE_GUID|  
|m_szDescription|DESCRIPTION|  
  
## Requirements  
 **Header:** atldbsch.h  
  
## See Also  
 [CRestrictions Class](../vs140/CRestrictions-Class.md)