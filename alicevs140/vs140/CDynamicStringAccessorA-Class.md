---
title: "CDynamicStringAccessorA Class"
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
ms.assetid: ed0d9821-a655-41f1-a902-43c3042ac49c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicStringAccessorA Class
Allows you to access a data source when you have no knowledge of the database schema (underlying structure).  
  
## Syntax  
  
```  
typedef CDynamicStringAccessorT<CHAR, DBTYPE_STR> CDynamicStringAccessorA;  
```  
  
## Remarks  
 They both request that the provider fetch all data accessed from the data store as string data, but `CDynamicStringAccessor` requests ANSI string data.  
  
 `CDynamicStringAccessorA` inherits **GetString** and `SetString` from `CDynamicStringAccessor`. When you use these methods in a `CDynamicStringAccessorA` object, ***BaseType*** is **CHAR**.  
  
## Requirements  
 **Header**: atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)   
 [CAccessor Class](../vs140/CAccessor-Class.md)   
 [CDynamicParameterAccessor Class](../vs140/CDynamicParameterAccessor-Class.md)   
 [CManualAccessor Class](../vs140/CManualAccessor-Class.md)   
 [CDynamicAccessor Class](../vs140/CDynamicAccessor-Class.md)   
 [CDynamicStringAccessor Class](../vs140/CDynamicStringAccessor-Class.md)