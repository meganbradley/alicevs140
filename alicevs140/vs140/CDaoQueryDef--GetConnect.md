---
title: "CDaoQueryDef::GetConnect"
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
ms.assetid: 250200d8-3530-4492-9b99-1b5ed2ad2fc0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetConnect
Call this member function to get the connection string associated with the querydef's data source.  
  
## Syntax  
  
```  
  
CString GetConnect( );  
  
```  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) containing the connection string for the querydef.  
  
## Remarks  
 This function is used only with ODBC data sources and certain ISAM drivers. It is not used with Microsoft Jet (.MDB) databases; in this case, `GetConnect` returns an empty string. For more information, see [SetConnect](../vs140/CDaoQueryDef--SetConnect.md).  
  
> [!TIP]
>  The preferred way to work with ODBC tables is to attach them to an .MDB database. For more information, see the topic "Accessing External Databases with DAO" in DAO Help.  
  
 For information about connection strings, see the topic "Connect Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)