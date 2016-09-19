---
title: "CDaoException::GetErrorInfo"
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
ms.assetid: 4183de78-d105-4b0c-81a9-68f1741e9e91
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoException::GetErrorInfo
Returns error information about a particular error object in the Errors collection.  
  
## Syntax  
  
```  
  
      void GetErrorInfo(  
   int nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 The index of the error information in the database engine's Errors collection, for lookup by index.  
  
## Remarks  
 Call this member function to obtain the following kinds of information about the exception:  
  
-   Error code  
  
-   Source  
  
-   Description  
  
-   Help file  
  
-   Help context  
  
 `GetErrorInfo` stores the information in the exception object's `m_pErrorInfo` data member. For a brief description of the information returned, see [m_pErrorInfo](../vs140/CDaoException--m_pErrorInfo.md). If you catch an exception of type `CDaoException` thrown by MFC, the `m_pErrorInfo` member will already be filled in. If you choose to call DAO directly, you must call the exception object's `GetErrorInfo` member function yourself to fill `m_pErrorInfo`. For a more detailed description, see the [CDaoErrorInfo](../vs140/CDaoErrorInfo-Structure.md) structure.  
  
 For information about DAO exceptions, and example code, see the article [Exceptions: Database Exceptions](../vs140/Exceptions--Database-Exceptions.md).  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoException Class](../vs140/CDaoException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoException::GetErrorCount](../vs140/CDaoException--GetErrorCount.md)