---
title: "CDatabase::SetLoginTimeout"
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
ms.assetid: 7a670f50-0481-4cb0-8e98-2cbe3bef23bc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::SetLoginTimeout
Call this member function — before you call `OpenEx` or **Open** — to override the default number of seconds allowed before an attempted data source connection times out.  
  
## Syntax  
  
```  
  
      void SetLoginTimeout(  
   DWORD dwSeconds   
);  
```  
  
#### Parameters  
 `dwSeconds`  
 The number of seconds to allow before a connection attempt times out.  
  
## Remarks  
 A connection attempt might time out if, for example, the DBMS is not available. Call **SetLoginTimeout** after you construct the uninitialized `CDatabase` object but before you call `OpenEx` or **Open**.  
  
 The default value for login timeouts is 15 seconds. Not all data sources support the ability to specify a login timeout value. If the data source does not support timeout, you get trace output but not an exception. A value of 0 means "infinite."  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::OnSetOptions](../vs140/CDatabase--OnSetOptions.md)   
 [CDatabase::SetQueryTimeout](../vs140/CDatabase--SetQueryTimeout.md)