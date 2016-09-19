---
title: "CDaoException::CDaoException"
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
ms.assetid: 018ab240-1724-4e29-a4de-f7a0cc9c534f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoException::CDaoException
Constructs a `CDaoException` object.  
  
## Syntax  
  
```  
  
CDaoException( );  
  
```  
  
## Remarks  
 Ordinarily, the framework creates exception objects when its code throws an exception. You seldom need to construct an exception object explicitly. If you want to throw a `CDaoException` from your own code, call the global function [AfxThrowDaoException](../vs140/AfxThrowDaoException.md).  
  
 However, you might want to explicitly create an exception object if you are making direct calls to DAO via the DAO interface pointers that MFC classes encapsulate. In that case, you might need to retrieve error information from DAO. Suppose an error occurs in DAO when you call a DAO method via the DAODatabases interface to a workspace's Databases collection.  
  
### To retrieve the DAO error information  
  
1.  Construct a `CDaoException` object.  
  
2.  Call the exception object's [GetErrorCount](../vs140/CDaoException--GetErrorCount.md) member function to determine how many error objects are in the database engine's Errors collection. (Normally only one, unless you are using an ODBC data source.)  
  
3.  Call the exception object's [GetErrorInfo](../vs140/CDaoException--GetErrorInfo.md) member function to retrieve one specific error object at a time, by index in the collection, via the exception object. Think of the exception object as a proxy for one DAO error object.  
  
4.  Examine the current [CDaoErrorInfo](../vs140/CDaoErrorInfo-Structure.md) structure that `GetErrorInfo` returns in the [m_pErrorInfo](../vs140/CDaoException--m_pErrorInfo.md) data member. Its members provide information on the DAO error.  
  
5.  In the case of an ODBC data source, repeat steps 3 and 4 as needed, for more error objects.  
  
6.  If you constructed the exception object on the heap, delete it with the **delete** operator when you finish.  
  
 For more information about handling errors in the MFC DAO classes, see the article [Exceptions: Database Exceptions](../vs140/Exceptions--Database-Exceptions.md).  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoException Class](../vs140/CDaoException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)