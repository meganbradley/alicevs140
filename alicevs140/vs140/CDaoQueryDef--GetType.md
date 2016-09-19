---
title: "CDaoQueryDef::GetType"
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
ms.assetid: 2ce9074e-4433-4a25-ace2-fc0ede22f293
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetType
Call this member function to determine the query type of the querydef.  
  
## Syntax  
  
```  
  
short GetType( );  
  
```  
  
## Return Value  
 The type of the query defined by the querydef. For values, see Remarks.  
  
## Remarks  
 The query type is set by what you specify in the querydef's SQL string when you create the querydef or call an existing querydef's [SetSQL](../vs140/CDaoQueryDef--SetSQL.md) member function. The query type returned by this function can be one of the following values:  
  
-   **dbQSelect** Select  
  
-   **dbQAction** Action  
  
-   **dbQCrosstab** Crosstab  
  
-   **dbQDelete** Delete  
  
-   **dbQUpdate** Update  
  
-   **dbQAppend** Append  
  
-   **dbQMakeTable** Make-table  
  
-   **dbQDDL** Data-definition  
  
-   **dbQSQLPassThrough** Pass-through  
  
-   **dbQSetOperation** Union  
  
-   **dbQSPTBulk** Used with **dbQSQLPassThrough** to specify a query that does not return records.  
  
> [!NOTE]
>  To create a SQL pass-through query, don't set the **dbSQLPassThrough** constant. This is set automatically by the Microsoft Jet database engine when you create a querydef object and set the connection string.  
  
 For information about SQL strings, see [GetSQL](../vs140/CDaoQueryDef--GetSQL.md). For information about query types, see [Execute](../vs140/CDaoQueryDef--Execute.md).  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)