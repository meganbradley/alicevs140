---
title: "CDaoException::GetErrorCount"
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
ms.assetid: 3d147cae-3baf-4f9f-a5d8-5df65053f02e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoException::GetErrorCount
Call this member function to retrieve the number of DAO error objects in the database engine's Errors collection.  
  
## Syntax  
  
```  
  
short GetErrorCount( );  
  
```  
  
## Return Value  
 The number of DAO error objects in the database engine's Errors collection.  
  
## Remarks  
 This information is useful for looping through the Errors collection to retrieve each of the one or more DAO error objects in the collection. To retrieve an error object by index or by DAO error number, call the [GetErrorInfo](../vs140/CDaoException--GetErrorInfo.md) member function.  
  
> [!NOTE]
>  Normally there is only one error object in the Errors collection. If you are working with an ODBC data source, however, there could be more than one.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoException Class](../vs140/CDaoException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)