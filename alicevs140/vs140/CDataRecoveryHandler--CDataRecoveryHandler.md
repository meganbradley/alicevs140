---
title: "CDataRecoveryHandler::CDataRecoveryHandler"
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
ms.assetid: 3984a1ff-68d3-4184-b6dd-7e3eb724bf83
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::CDataRecoveryHandler
Constructs a `CDataRecoveryHandler` object.  
  
## Syntax  
  
```  
CDataRecoveryHandler(  
   DWORD dwRestartManagerSupportFlags,  
   int nAutosaveInterval  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `dwRestartManagerSupportFlags`|Indicates which options of the restart manager are supported.|  
|[in] `nAutosaveInterval`|The time between autosaves. This parameter is in milliseconds.|  
  
## Remarks  
 The MFC framework automatically creates a `CDataRecoveryHandler` object for your application when you use the **New Project** wizard. Unless you are customizing the data recovery behavior or the restart manager, you should not create a `CDataRecoveryHandler` object.  
  
 For more information about the support flags, see [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md).  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)