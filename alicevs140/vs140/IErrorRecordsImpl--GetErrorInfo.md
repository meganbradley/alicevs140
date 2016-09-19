---
title: "IErrorRecordsImpl::GetErrorInfo"
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
ms.assetid: 44d0872f-f25f-4102-8f7f-a2cfb3eeb1a0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IErrorRecordsImpl::GetErrorInfo
Returns an [IErrorInfo](https://msdn.microsoft.com/en-us/library/ms718112.aspx) interface pointer on the specified record.  
  
## Syntax  
  
```  
  
      STDMETHOD( GetErrorInfo )(  
   ULONG ulRecordNum,  
   LCID lcid,  
   IErrorInfo **ppErrorInfo   
);  
```  
  
#### Parameters  
 See [IErrorRecords::GetErrorInfo](https://msdn.microsoft.com/en-us/library/ms711230.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IErrorRecordsImpl Class](../vs140/IErrorRecordsImpl-Class.md)