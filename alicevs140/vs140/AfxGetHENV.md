---
title: "AfxGetHENV"
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
ms.assetid: d8be2a8e-b93a-460f-affb-cf65b2f3dc10
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetHENV
You can use the returned handle in direct ODBC calls, but you must not close the handle or assume that the handle is still valid and available after any existing `CDatabase`- or `CRecordset`-derived objects have been destroyed.  
  
## Syntax  
  
```  
  
HENV AFXAPI AfxGetHENV( );  
  
```  
  
## Return Value  
 The handle to the ODBC environment currently in use by MFC. Can be `SQL_HENV_NULL` if there are no [CDatabase](../vs140/CDatabase-Class.md) objects and no [CRecordset](../vs140/CRecordset-Class.md) objects in use.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)