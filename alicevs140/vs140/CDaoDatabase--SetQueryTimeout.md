---
title: "CDaoDatabase::SetQueryTimeout"
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
ms.assetid: d7649daf-ec04-464a-88ec-6ad88bdf4bd0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::SetQueryTimeout
Call this member function to override the default number of seconds to allow before subsequent operations on the connected database time out.  
  
## Syntax  
  
```  
  
      void SetQueryTimeout(   
   short nSeconds    
);  
```  
  
#### Parameters  
 `nSeconds`  
 The number of seconds to allow before a query attempt times out.  
  
## Remarks  
 An operation might time out because of network access problems, excessive query processing time, and so on. Call `SetQueryTimeout` before opening your recordset or before calling the recordset's [AddNew](../vs140/CDaoRecordset--AddNew.md), [Update](../vs140/CDaoRecordset--Update.md), or [Delete](../vs140/CDaoRecordset--Delete.md) member functions if you want to change the query timeout value. The setting affects all subsequent [Open](../vs140/CDaoRecordset--Open.md), `AddNew`, **Update**, and **Delete** calls to any recordsets associated with this `CDaoDatabase` object. Changing the query timeout value for a recordset after opening does not change the value for the recordset. For example, subsequent [Move](../vs140/CDaoRecordset--Move.md) operations do not use the new value.  
  
 The default value for query timeouts is 60 seconds. Not all databases support the ability to set a query timeout value. If you set a query timeout value of 0, no timeout occurs; the communication with the database may stop responding. This behavior may be useful during development.  
  
 For related information, see the topic "QueryTimeout Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoWorkspace::SetLoginTimeout](../vs140/CDaoWorkspace--SetLoginTimeout.md)