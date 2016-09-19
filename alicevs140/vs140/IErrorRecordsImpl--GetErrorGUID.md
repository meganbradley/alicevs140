---
title: "IErrorRecordsImpl::GetErrorGUID"
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
ms.assetid: 42c00755-50e5-401a-8246-adef9de5ced2
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IErrorRecordsImpl::GetErrorGUID
Gets the error GUID from an error record.  
  
## Syntax  
  
```  
  
      REFGUID GetErrorGUID(  
   ERRORINFO& rCurError   
);  
```  
  
#### Parameters  
 `rCurError`  
 An `ERRORINFO` record in an **IErrorInfo** interface.  
  
## Return Value  
 A reference to a GUID for the error.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IErrorRecordsImpl Class](../vs140/IErrorRecordsImpl-Class.md)