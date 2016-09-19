---
title: "CDataConnection::operator bool (OLE DB)"
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
ms.assetid: e0791faf-2ed2-4dbb-9e68-3b9b5da2b7a7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataConnection::operator bool (OLE DB)
Determines whether the current session is open or not.  
  
## Syntax  
  
```  
  
operator bool( ) throw( );  
  
```  
  
## Remarks  
 Returns a `bool` (C++ data type) value. **true** means the current session is open; **false** means the current session is closed.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDataConnection Class](../vs140/CDataConnection-Class.md)   
 [CDataConnection::operator BOOL](../vs140/CDataConnection--operator-BOOL.md)