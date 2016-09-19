---
title: "IErrorRecordsImpl::AddErrorRecord"
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
ms.assetid: b5f8e9ae-509d-454f-b511-4bda7e972607
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IErrorRecordsImpl::AddErrorRecord
Adds a record to the OLE DB error object.  
  
## Syntax  
  
```  
  
      STDMETHOD( AddErrorRecord )(  
   ERRORINFO *pErrorInfo,  
   DWORD dwLookupID,  
   DISPPARAMS *pdispparams,  
   IUnknown *punkCustomError,  
   DWORD dwDynamicErrorID   
);  
```  
  
#### Parameters  
 See [IErrorRecords::AddErrorRecord](https://msdn.microsoft.com/en-us/library/ms725362.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IErrorRecordsImpl Class](../vs140/IErrorRecordsImpl-Class.md)