---
title: "Are DDL and DML Supported?"
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
ms.assetid: 07f96d81-78d4-4bec-9138-b15d68fd5ce0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Are DDL and DML Supported?
The MFC DAO classes support two kinds of access to databases:  
  
-   **Data definition language (DDL)** You can create and delete databases, create and delete tables, define table fields and indexes, and take other actions that affect the structure of your database.  
  
-   **Data manipulation language (DML)** You can run queries, add, delete, and edit records, and otherwise manipulate the content of your database.  
  
 The MFC ODBC classes support only DML, but you can call ODBC API functions directly to carry out DDL tasks.  
  
## See Also  
 [Data Access Frequently Asked Questions](../vs140/Data-Access-Frequently-Asked-Questions---MFC-Data-Access-.md)