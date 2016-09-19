---
title: "CDatabase::Close"
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
ms.assetid: 8e56eb8d-784b-4816-9c0e-417650310208
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::Close
Call this member function if you want to disconnect from a data source.  
  
## Syntax  
  
```  
  
virtual void Close( );  
```  
  
## Remarks  
 You must close any recordsets associated with the `CDatabase` object before you call this member function. Because **Close** does not destroy the `CDatabase` object, you can reuse the object by opening a new connection to the same data source or a different data source.  
  
 All pending `AddNew` or **Edit** statements of recordsets using the database are canceled, and all pending transactions are rolled back. Any recordsets dependent on the `CDatabase` object are left in an undefined state.  
  
## Example  
 [!CODE [NVC_MFCDatabase#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#12)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::OpenEx](../vs140/CDatabase--OpenEx.md)   
 [CDatabase::Open](../vs140/CDatabase--Open.md)