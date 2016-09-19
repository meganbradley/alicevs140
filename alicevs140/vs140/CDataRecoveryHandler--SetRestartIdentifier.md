---
title: "CDataRecoveryHandler::SetRestartIdentifier"
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
ms.assetid: 33c0fea6-e2c7-48a4-9c7e-8cfededaee67
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::SetRestartIdentifier
Sets the unique restart identifier for this instance of the `CDataRecoveryHandler`.  
  
## Syntax  
  
```  
virtual void SetRestartIdentifier(  
   const CString &strRestartIdentifier  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `strRestartIdentifier`|The unique identifier for the restart manager.|  
  
## Remarks  
 The restart manager records information about the open documents in the registry. This information is stored with the unique restart identifier as the key. Because the restart identifier is unique for each instance of an application, multiple instances of an application may exit unexpectedly and the restart manager can recover each of them.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::GetRestartIdentifier](../vs140/CDataRecoveryHandler--GetRestartIdentifier.md)