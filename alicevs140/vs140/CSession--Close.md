---
title: "CSession::Close"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dc36c4c0-e588-4c0b-91d1-fc7dc5c8e7f4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSession::Close
Closes the session, which was opened by [CSession::Open](../vs140/CSession--Open.md).  
  
## Syntax  
  
```  
  
void Close( ) throw( );  
  
```  
  
## Remarks  
 Releases the **m_spOpenRowset** pointer.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CSession Class](../vs140/CSession-Class.md)