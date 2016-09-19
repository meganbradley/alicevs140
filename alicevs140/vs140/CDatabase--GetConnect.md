---
title: "CDatabase::GetConnect"
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
ms.assetid: e90600aa-6758-40f9-ac90-9ac2309fbfcf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::GetConnect
Call this member function to retrieve the connection string used during the call to `OpenEx` or `Open` that connected the `CDatabase` object to a data source.  
  
## Syntax  
  
```  
const CString GetConnect( ) const;  
```  
  
## Return Value  
 A `const`[CString](../vs140/CStringT-Class.md) containing the connection string if `OpenEx` or `Open` has been called; otherwise, an empty string.  
  
## Remarks  
 See [CDatabase::Open](../vs140/CDatabase--Open.md) for a description of how the connection string is created.  
  
## Requirements  
 Header: afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::OpenEx](../vs140/CDatabase--OpenEx.md)   
 [CDatabase::Open](../vs140/CDatabase--Open.md)