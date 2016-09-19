---
title: "CSession::Abort"
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
ms.assetid: 02413b20-c486-451f-b4d7-73a6e8065df8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSession::Abort
Terminates the transaction.  
  
## Syntax  
  
```  
  
      HRESULT Abort(   
   BOID* pboidReason = NULL,   
   BOOL bRetaining = FALSE,   
   BOOL bAsync = FALSE    
) const throw( );  
```  
  
#### Parameters  
 See [ITransaction::Abort](https://msdn.microsoft.com/en-us/library/ms709833.aspx) in the *OLE DB Programmer's Reference*.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CSession Class](../vs140/CSession-Class.md)