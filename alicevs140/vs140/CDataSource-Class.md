---
title: "CDataSource Class"
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
ms.assetid: 99bf862c-9d5c-4117-9501-aa0e2672085c
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataSource Class
Corresponds to an OLE DB data source object, which represents a connection through a provider to a data source.  
  
## Syntax  
  
```  
class CDataSource  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[Close](../vs140/CDataSource--Close.md)|Closes the connection.|  
|[GetInitializationString](../vs140/CDataSource--GetInitializationString.md)|Retrieves the initialization string of the data source that is currently open.|  
|[GetProperties](../vs140/CDataSource--GetProperties.md)|Gets the values of properties currently set for the connected data source.|  
|[GetProperty](../vs140/CDataSource--GetProperty.md)|Gets the value of a single property currently set for the connected data source.|  
|[Open](../vs140/CDataSource--Open.md)|Creates a connection to a provider (data source) using either a **CLSID**, **ProgID**, or a `CEnumerator` moniker provided by the caller.|  
|[OpenFromFileName](../vs140/CDataSource--OpenFromFileName.md)|Opens a data source from a file specified by the user-supplied file name.|  
|[OpenFromInitializationString](../vs140/CDataSource--OpenFromInitializationString.md)|Opens the data source specified by an initialization string.|  
|[OpenWithPromptFileName](../vs140/CDataSource--OpenWithPromptFileName.md)|Allows the user to select a previously created data link file to open the corresponding data source.|  
|[OpenWithServiceComponents](../vs140/CDataSource--OpenWithServiceComponents.md)|Opens a data source object using the Data Link dialog box.|  
  
## Remarks  
 One or more database sessions can be created for a single connection. These sessions are represented by `CSession`. You must call [CDataSource::Open](../vs140/CDataSource--Open.md) to open the connection before creating a session with `CSession::Open`.  
  
 For an example of how to use `CDataSource`, see the [CatDB](../vs140/Visual-C---Samples.md) sample.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)