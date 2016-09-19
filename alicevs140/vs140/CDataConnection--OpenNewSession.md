---
title: "CDataConnection::OpenNewSession"
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
ms.assetid: 0a70e573-9498-4ca7-b524-45666dc7b0a3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataConnection::OpenNewSession
Opens a new session using the current connection object's data source.  
  
## Syntax  
  
```  
  
      HRESULT OpenNewSession(   
   CSession & session    
) throw( );  
```  
  
#### Parameters  
 `session`  
 [in/out] A reference to the new session object.  
  
 **Remarks**  
 The new session uses the current connection object's contained data source object as its parent, and can access all of the same information as the data source.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDataConnection Class](../vs140/CDataConnection-Class.md)