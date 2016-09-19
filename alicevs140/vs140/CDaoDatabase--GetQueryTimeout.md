---
title: "CDaoDatabase::GetQueryTimeout"
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
ms.assetid: ead14f3a-f3f5-4cce-ab9e-5da36114cb0f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::GetQueryTimeout
Call this member function to retrieve the current number of seconds to allow before subsequent operations on the connected database are timed out.  
  
## Syntax  
  
```  
  
short GetQueryTimeout( );  
  
```  
  
## Return Value  
 A short integer containing the timeout value in seconds.  
  
## Remarks  
 An operation might time out due to network access problems, excessive query processing time, and so on. While the setting is in effect, it affects all open, add new, update, and delete operations on any recordsets associated with this `CDaoDatabase` object. You can change the current timeout setting by calling [SetQueryTimeout](../vs140/CDaoDatabase--SetQueryTimeout.md). Changing the query timeout value for a recordset after opening does not change the value for the recordset. For example, subsequent [Move](../vs140/CDaoRecordset--Move.md) operations do not use the new value. The default value is initially set when the database engine is initialized.  
  
 The default value for query timeouts is taken from the Windows registry. If there is no registry setting, the default is 60 seconds. Not all databases support the ability to set a query timeout value. If you set a query timeout value of 0, no timeout occurs; and communication with the database may stop responding. This behavior may be useful during development. If the call fails, MFC throws an exception of type [CDaoException](../vs140/CDaoException-Class.md).  
  
 For related information, see the topic "QueryTimeout Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoWorkspace::SetLoginTimeout](../vs140/CDaoWorkspace--SetLoginTimeout.md)