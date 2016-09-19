---
title: "CDaoQueryDef::SetConnect"
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
ms.assetid: 3b21f237-4162-4756-b12e-a8b7a72b9ae1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::SetConnect
Call this member function to set the querydef object's connection string.  
  
## Syntax  
  
```  
  
      void SetConnect(   
   LPCTSTR lpszConnect    
);  
```  
  
#### Parameters  
 `lpszConnect`  
 A string that contains a connection string for the associated [CDaoDatabase](../vs140/CDaoDatabase-Class.md) object.  
  
## Remarks  
 The connection string is used to pass additional information to ODBC and certain ISAM drivers as needed. It is not used for Microsoft Jet (.MDB) databases.  
  
> [!TIP]
>  The preferred way to work with ODBC tables is to attach them to an .MDB database.  
  
 Before executing a querydef that represents a SQL pass-through query to an ODBC data source, set the connection string with `SetConnect` and call [SetReturnsRecords](../vs140/CDaoQueryDef--SetReturnsRecords.md) to specify whether the query returns records.  
  
 For more information about the connection string's structure and examples of connection string components, see the topic "Connect Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)