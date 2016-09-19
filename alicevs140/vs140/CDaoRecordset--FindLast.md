---
title: "CDaoRecordset::FindLast"
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
ms.assetid: 96e737f2-5faf-422a-9c20-ee43a40b3353
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::FindLast
Call this member function to find the last record that matches a specified condition.  
  
## Syntax  
  
```  
  
      BOOL FindLast(  
   LPCTSTR lpszFilter   
);  
```  
  
#### Parameters  
 `lpszFilter`  
 A string expression (like the **WHERE** clause in a SQL statement without the word **WHERE**) used to locate the record.  
  
## Return Value  
 Nonzero if matching records are found, otherwise 0.  
  
## Remarks  
 The `FindLast` member function begins its search at the end of the recordset and searches backward towards the beginning of the recordset.  
  
 If you want to include all the records in your search (not just those that meet a specific condition) use one of the Move operations to move from record to record. To locate a record in a table-type recordset, call the `Seek` member function.  
  
 If a record matching the criteria is not located, the current record pointer is undetermined, and `FindLast` returns zero. If the recordset contains more than one record that satisfies the criteria, `FindFirst` locates the first occurrence, `FindNext` locates the next occurrence after the first occurrence, and so on.  
  
> [!CAUTION]
>  If you edit the current record, be sure you save the changes by calling the **Update** member function before you move to another record. If you move to another record without updating, your changes are lost without warning.  
  
 Using one of the Find operations is not the same as calling **MoveFirst** or `MoveNext`, however, which simply makes the first or next record current without specifying a condition. You can follow a Find operation with a Move operation.  
  
 Keep the following in mind when using the Find operations:  
  
-   If **Find** returns nonzero, the current record is not defined. In this case, you must position the current record pointer back to a valid record.  
  
-   You cannot use a Find operation with a forward-only scrolling snapshot-type recordset.  
  
-   You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you are not using the U.S. version of the Microsoft Jet database engine; otherwise, matching records may not be found.  
  
-   When working with ODBC databases and large dynasets, you may discover that using the Find operations is slow, especially when working with large recordsets. You can improve performance by using SQL queries with customized **ORDER BY** or **WHERE** clauses, parameter queries, or **CDaoQuerydef** objects that retrieve specific indexed records.  
  
 For related information, see the topic "FindFirst, FindLast, FindNext, FindPrevious Methods" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::Find](../vs140/CDaoRecordset--Find.md)   
 [CDaoRecordset::FindFirst](../vs140/CDaoRecordset--FindFirst.md)   
 [CDaoRecordset::FindNext](../vs140/CDaoRecordset--FindNext.md)   
 [CDaoRecordset::FindPrev](../vs140/CDaoRecordset--FindPrev.md)