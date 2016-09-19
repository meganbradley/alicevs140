---
title: "CSession Class"
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
ms.assetid: 83cd798f-b45d-4f11-a23c-29183390450c
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSession Class
Represents a single database access session.  
  
## Syntax  
  
```  
class CSession  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[Abort](../vs140/CSession--Abort.md)|Cancels (terminates) the transaction.|  
|[Close](../vs140/CSession--Close.md)|Closes the session.|  
|[Commit](../vs140/CSession--Commit.md)|Commits the transaction.|  
|[GetTransactionInfo](../vs140/CSession--GetTransactionInfo.md)|Returns information regarding a transaction.|  
|[Open](../vs140/CSession--Open.md)|Opens a new session for the data source object.|  
|[StartTransaction](../vs140/CSession--StartTransaction.md)|Begins a new transaction for this session.|  
  
## Remarks  
 One or more sessions can be associated with each provider connection (data source), which is represented by a [CDataSource](../vs140/CDataSource-Class.md) object. To create a new `CSession` for a `CDataSource`, call [CSession::Open](../vs140/CSession--Open.md). To begin a database transaction, `CSession` provides the `StartTransaction` method. Once a transaction is started, you can commit to it using the **Commit** method, or cancel it using the **Abort** method.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CatDB](../vs140/Visual-C---Samples.md)   
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)