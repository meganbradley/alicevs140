---
title: "AfxThrowDBException"
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
ms.assetid: f086d61b-56dc-4d3a-a273-b3c62986e195
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxThrowDBException
Call this function to throw an exception of type `CDBException` from your own code.  
  
## Syntax  
  
```  
  
      void AfxThrowDBException(  
   RETCODE nRetCode,  
   CDatabase* pdb,  
   HSTMT hstmt   
);  
```  
  
#### Parameters  
 `nRetCode`  
 A value of type **RETCODE**, defining the type of error that caused the exception to be thrown.  
  
 `pdb`  
 A pointer to the `CDatabase` object that represents the data source connection with which the exception is associated.  
  
 `hstmt`  
 An ODBC **HSTMT** handle that specifies the statement handle with which the exception is associated.  
  
## Remarks  
 The framework calls `AfxThrowDBException` when it receives an ODBC **RETCODE** from a call to an ODBC API function and interprets the **RETCODE** as an exceptional condition rather than an expectable error. For example, a data access operation might fail because of a disk read error.  
  
 For information about the **RETCODE** values defined by ODBC, see Chapter 8, "Retrieving Status and Error Information," in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For information about MFC extensions to these codes, see class [CDBException](../vs140/CDBException-Class.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CDBException::m_nRetCode](../vs140/CDBException--m_nRetCode.md)