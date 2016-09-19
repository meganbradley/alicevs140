---
title: "CDaoRecordset::Find"
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
ms.assetid: b2ad1564-7958-453a-98ce-43eb9c5f2eb2
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::Find
Call this member function to locate a particular string in a dynaset- or snapshot-type recordset using a comparison operator.  
  
## Syntax  
  
```  
  
      virtual BOOL Find(  
   long lFindType,  
   LPCTSTR lpszFilter   
);  
```  
  
#### Parameters  
 *lFindType*  
 A value indicating the type of Find operation desired. The possible values are:  
  
-   **AFX_DAO_NEXT** Find the next location of a matching string.  
  
-   **AFX_DAO_PREV** Find the previous location of a matching string.  
  
-   **AFX_DAO_FIRST** Find the first location of a matching string.  
  
-   **AFX_DAO_LAST** Find the last location of a matching string.  
  
 `lpszFilter`  
 A string expression (like the **WHERE** clause in a SQL statement without the word **WHERE**) used to locate the record. For example:  
  
 [!CODE [NVC_MFCDatabase#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#3)]  
  
## Return Value  
 Nonzero if matching records are found, otherwise 0.  
  
## Remarks  
 You can find the first, next, previous, or last instance of the string. **Find** is a virtual function, so you can override it and add your own implementation. The `FindFirst`, `FindLast`, `FindNext`, and `FindPrev` member functions call the **Find** member function, so you can use **Find** to control the behavior of all Find operations.  
  
 To locate a record in a table-type recordset, call the [Seek](../vs140/CDaoRecordset--Seek.md) member function.  
  
> [!TIP]
>  The smaller the set of records you have, the more effective **Find** will be. In general, and especially with ODBC data, it is better to create a new query that retrieves just the records you want.  
  
 For related information, see the topic "FindFirst, FindLast, FindNext, FindPrevious Methods" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::FindFirst](../vs140/CDaoRecordset--FindFirst.md)   
 [CDaoRecordset::FindLast](../vs140/CDaoRecordset--FindLast.md)   
 [CDaoRecordset::FindNext](../vs140/CDaoRecordset--FindNext.md)   
 [CDaoRecordset::FindPrev](../vs140/CDaoRecordset--FindPrev.md)