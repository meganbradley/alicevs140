---
title: "CSession::Open"
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
ms.assetid: c2050c2c-9817-4857-be49-189f346968f6
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSession::Open
Opens a new session for the data source object.  
  
## Syntax  
  
```  
  
      HRESULT Open(  
   const CDataSource& ds,  
   DBPROPSET *pPropSet = NULL,  
   ULONG ulPropSets = 0  
) throw( );  
```  
  
#### Parameters  
 `ds`  
 [in] The data source for which the session is to be opened.  
  
 *pPropSet*  
 [in] A pointer to an array of [DBPROPSET](https://msdn.microsoft.com/en-us/library/ms714367.aspx) structures containing properties and values to be set. See [Property Sets and Property Groups](https://msdn.microsoft.com/en-us/library/ms713696.aspx) in the *OLE DB Programmer's Reference* in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `ulPropSets`  
 [in] The number of [DBPROPSET](https://msdn.microsoft.com/en-us/library/ms714367.aspx) structures passed in the *pPropSet* argument.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 You must open the data source object using [CDataSource::Open](../vs140/CDataSource--Open.md) before passing it to `CSession::Open`.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CSession Class](../vs140/CSession-Class.md)