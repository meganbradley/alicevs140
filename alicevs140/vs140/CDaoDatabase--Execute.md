---
title: "CDaoDatabase::Execute"
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
ms.assetid: e9de6744-9f9d-4106-af72-207387f627de
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::Execute
Call this member function to run an action query or execute a SQL statement on the database.  
  
## Syntax  
  
```  
  
      void Execute(   
   LPCTSTR lpszSQL,   
   int nOptions = dbFailOnError    
);  
```  
  
#### Parameters  
 `lpszSQL`  
 Pointer to a null-terminated string containing a valid SQL command to execute.  
  
 `nOptions`  
 An integer that specifies options relating to the integrity of the query. You can use the bitwise-OR operator (**&#124;**) to combine any of the following constants (provided the combination makes sense — for example, you would not combine **dbInconsistent** with **dbConsistent**):  
  
-   **dbDenyWrite** Deny write permission to other users.  
  
-   **dbInconsistent** (Default) Inconsistent updates.  
  
-   **dbConsistent** Consistent updates.  
  
-   **dbSQLPassThrough** SQL pass-through. Causes the SQL statement to be passed to an ODBC data source for processing.  
  
-   **dbFailOnError** Roll back updates if an error occurs.  
  
-   **dbSeeChanges** Generate a run-time error if another user is changing data you are editing.  
  
> [!NOTE]
>  If both **dbInconsistent** and **dbConsistent** are included or if neither is included, the result is the default. For an explanation of these constants, see the topic "Execute Method" in DAO Help.  
  
## Remarks  
 **Execute** works only for action queries or SQL pass-through queries that do not return results. It does not work for select queries, which return records.  
  
 For a definition and information about action queries, see the topics "Action Query" and "Execute Method" in DAO Help.  
  
> [!TIP]
>  Given a syntactically correct SQL statement and proper permissions, the **Execute** member function will not fail even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** member function to run an update or delete query. This option causes MFC to throw an exception of type [CDaoException](../vs140/CDaoException-Class.md) and rolls back all successful changes if any of the records affected are locked and cannot be updated or deleted. Note that you can always call `GetRecordsAffected` to see how many records were affected.  
  
 Call the [GetRecordsAffected](../vs140/CDaoDatabase--GetRecordsAffected.md) member function of the database object to determine the number of records affected by the most recent **Execute** call. For example, `GetRecordsAffected` returns information about the number of records deleted, updated, or inserted when executing an action query. The count returned will not reflect changes in related tables when cascade updates or deletes are in effect.  
  
 **Execute** does not return a recordset. Using **Execute** on a query that selects records causes MFC to throw an exception of type `CDaoException`. (There is no `ExecuteSQL` member function analogous to `CDatabase::ExecuteSQL`.)  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)