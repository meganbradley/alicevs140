---
title: "ODBC Driver Requirements for Dynasets"
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
ms.assetid: 585cc67b-4d92-404b-9903-d769cd17badc
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ODBC Driver Requirements for Dynasets
In the MFC ODBC database classes, dynasets are recordsets with dynamic properties; they remain synchronized with the data source in certain ways. MFC dynasets (but not forward-only recordsets) require an ODBC driver with Level 2 API conformance. If the driver for your [data source](../vs140/Data-Source--ODBC-.md) conforms to the Level 1 API set, you can still use both updateable and read-only snapshots and forward-only recordsets, but not dynasets. However, a Level 1 driver can support dynasets if it supports extended fetch and keyset-driven cursors.  
  
 In ODBC terminology, dynasets and snapshots are referred to as cursors. A cursor is a mechanism used for keeping track of its position in a recordset. For more information about driver requirements for dynasets, see [Dynaset](../vs140/Dynaset.md). For more information about cursors, see the [Open Database Connectivity (ODBC)](https://msdn.microsoft.com/en-us/library/ms710252.aspx) SDK in the MSDN documentation.  
  
> [!NOTE]
>  For updateable recordsets, your ODBC driver must support either positioned update statements or the **::SQLSetPos** ODBC API function. If both are supported, MFC uses **::SQLSetPos** for efficiency. Alternatively, for snapshots, you can use the cursor library, which provides the required support for updateable snapshots (static cursors and positioned update statements).  
  
## See Also  
 [ODBC Basics](../vs140/ODBC-Basics.md)