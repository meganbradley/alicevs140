---
title: "CAsyncMonikerFile::OnDataAvailable"
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
ms.assetid: 0d349d71-4f5a-443f-8f5d-33a3e17e8863
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncMonikerFile::OnDataAvailable
An asynchronous moniker calls `OnDataAvailable` to provide data to the client as it becomes available, during asynchronous bind operations.  
  
## Syntax  
  
```  
  
      virtual void OnDataAvailable(   
   DWORD dwSize,   
   DWORD bscfFlag    
);  
```  
  
#### Parameters  
 `dwSize`  
 The cumulative amount (in bytes) of data available since the beginning of the binding. Can be zero, indicating that the amount of data is not relevant to the operation, or that no specific amount became available.  
  
 *bscfFlag*  
 A **BSCF** enumeration value. Can be one or more of the following values:  
  
-   **BSCF_FIRSTDATANOTIFICATION** Identifies the first call to `OnDataAvailable` for a given bind operation.  
  
-   **BSCF_INTERMEDIATEDATANOTIFICATION** Identifies an intermediary call to `OnDataAvailable` for a bind operation.  
  
-   **BSCF_LASTDATANOTIFICATION** Identifies the last call to `OnDataAvailable` for a bind operation.  
  
## Remarks  
 The default implementation of this function does nothing. See the following example for a sample implementation.  
  
## Example  
 [!CODE [NVC_MFCWinInet#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWinInet#5)]  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CAsyncMonikerFile Class](../vs140/CAsyncMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataPathProperty Class](../vs140/CDataPathProperty-Class.md)