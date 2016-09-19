---
title: "CDataConnection Class"
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
ms.assetid: 77432d85-4e20-49ec-a0b0-142137828471
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataConnection Class
Manages the connection with the data source.  
  
## Syntax  
  
```  
class CDataConnection  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[CDataConnection](../vs140/CDataConnection--CDataConnection.md)|Constructor. Instantiates and initializes a `CDataConnection` object.|  
|[Copy](../vs140/CDataConnection--Copy.md)|Creates a copy of an existing data connection.|  
|[Open](../vs140/CDataConnection--Open.md)|Opens a connection to a data source using an initialization string.|  
|[OpenNewSession](../vs140/CDataConnection--OpenNewSession.md)|Opens a new session on the current connection.|  
  
### Operators  
  
|||  
|-|-|  
|[operator BOOL](../vs140/CDataConnection--operator-BOOL.md)|Determines whether the current session is open or not.|  
|[operator bool](../vs140/CDataConnection--operator-bool--OLE-DB-.md)|Determines whether the current session is open or not.|  
|[operator CDataSource&](../vs140/CDataConnection--operator-CDataSource-.md)|Returns a reference to the contained `CDataSource` object.|  
|[operator CDataSource*](../vs140/CDataConnection--operator-CDataSource-.md)|Returns a pointer to the contained `CDataSource` object.|  
|[operator CSession&](../vs140/CDataConnection--operator-CSession-.md)|Returns a reference to the contained `CSession` object.|  
|[operator CSession*](../vs140/CDataConnection--operator-CSession-.md)|Returns a pointer to the contained `CSession` object.|  
  
## Remarks  
 `CDataConnection` is a useful class for creating clients because it encapsulates necessary objects (data source and session) and some of the work you need to do when connecting to a data source  
  
 Without `CDataConnection`, you have to create a `CDataSource` object, call its [OpenFromInitializationString](../vs140/CDataSource--OpenFromInitializationString.md) method, then create an instance of a [CSession](../vs140/CSession-Class.md) object, call its [Open](../vs140/CSession--Open.md) method, then create a [CCommand](../vs140/CCommand-Class.md) object and call its **Open*** methods.  
  
 With `CDataConnection`, you only need to create a connection object, pass it an initialization string, then use that connection to open commands. If you plan on using your connection to the database repeatedly, it is a good idea to keep the connection open, and `CDataConnection` provides a convenient way to do that.  
  
> [!NOTE]
>  If you are creating a database application that needs to handle multiple sessions, you will need to use [OpenNewSession](../vs140/CDataConnection--OpenNewSession.md).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)