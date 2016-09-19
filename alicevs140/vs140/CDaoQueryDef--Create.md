---
title: "CDaoQueryDef::Create"
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
ms.assetid: b17c072a-f6ad-4011-a093-7904f6815b42
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::Create
Call this member function to create a new saved query or a new temporary query.  
  
## Syntax  
  
```  
  
      virtual void Create(   
   LPCTSTR lpszName = NULL,   
   LPCTSTR lpszSQL = NULL    
);  
```  
  
#### Parameters  
 `lpszName`  
 The unique name of the query saved in the database. For details about the string, see the topic "CreateQueryDef Method" in DAO Help. If you accept the default value, an empty string, a temporary querydef is created. Such a query is not saved in the QueryDefs collection.  
  
 `lpszSQL`  
 The SQL string that defines the query. If you accept the default value of **NULL**, you must later call [SetSQL](../vs140/CDaoQueryDef--SetSQL.md) to set the string. Until then, the query is undefined. You can, however, use the undefined query to open a recordset; see Remarks for details. The SQL statement must be defined before you can append the querydef to the QueryDefs collection.  
  
## Remarks  
 If you pass a name in `lpszName`, you can then call [Append](../vs140/CDaoQueryDef--Append.md) to save the querydef in the database's QueryDefs collection. Otherwise, the object is a temporary querydef and is not saved. In either case, the querydef is in an open state, and you can either use it to create a [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object or call the querydef's [Execute](../vs140/CDaoQueryDef--Execute.md) member function.  
  
 If you do not supply a SQL statement in `lpszSQL`, you cannot run the query with **Execute** but you can use it to create a recordset. In that case, MFC uses the recordset's default SQL statement.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::Open](../vs140/CDaoQueryDef--Open.md)   
 [CDaoQueryDef::CDaoQueryDef](../vs140/CDaoQueryDef--CDaoQueryDef.md)   
 [CDaoRecordset::GetSQL](../vs140/CDaoRecordset--GetSQL.md)