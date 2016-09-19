---
title: "IWorkerThreadClient::CloseHandle"
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
ms.assetid: 0b424eaa-13be-489e-831e-fec518d48e7d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IWorkerThreadClient::CloseHandle
Implement this method to close the handle associated with this object.  
  
## Syntax  
  
```  
  
      HRESULT CloseHandle(  
   HANDLE hHandle   
);  
```  
  
#### Parameters  
 *hHandle*  
 The handle to be closed.  
  
## Return Value  
 Return S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 The handle passed to this method was previously associated with this object by a call to [CWorkerThread::AddHandle](../vs140/CWorkerThread--AddHandle.md).  
  
## Example  
 The following code shows a simple implementation of `IWorkerThreadClient::CloseHandle`.  
  
 [!CODE [NVC_ATL_Utilities#135](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#135)]  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [IWorkerThreadClient Interface](../vs140/IWorkerThreadClient-Interface.md)   
 [CWorkerThread::AddHandle](../vs140/CWorkerThread--AddHandle.md)