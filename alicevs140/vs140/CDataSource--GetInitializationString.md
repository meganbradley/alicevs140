---
title: "CDataSource::GetInitializationString"
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
ms.assetid: 97134723-6e99-4004-a56d-ec57543dbf3b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataSource::GetInitializationString
Retrieves the initialization string of a data source that is currently open.  
  
## Syntax  
  
```  
  
      HRESULT GetInitializationString(   
   BSTR* pInitializationString,   
   bool bIncludePassword = false    
) throw( );  
```  
  
#### Parameters  
 *pInitializationString*  
 [out] A pointer to the initialization string.  
  
 *bIncludePassword*  
 [in] **true** if string includes a password; otherwise **false**.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 The resulting initialization string can be used to later reopen this data source connection.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDataSource Class](../vs140/CDataSource-Class.md)