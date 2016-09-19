---
title: "IWorkerThreadClient::Execute"
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
ms.assetid: 86e156d6-1f65-400a-9a1e-640b8b638bd8
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IWorkerThreadClient::Execute
Implement this method to execute code when the handle associated with this object becomes signaled.  
  
## Syntax  
  
```  
  
      HRESULT Execute(  
   DWORD_PTR dwParam,  
   HANDLE hObject   
);  
```  
  
#### Parameters  
 `dwParam`  
 The user parameter.  
  
 `hObject`  
 The handle that has become signaled.  
  
## Return Value  
 Return S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 The handle and DWORD/pointer passed to this method were previously associated with this object by a call to [CWorkerThread::AddHandle](../vs140/CWorkerThread--AddHandle.md).  
  
## Example  
 The following code shows a simple implementation of `IWorkerThreadClient::Execute`.  
  
 [!CODE [NVC_ATL_Utilities#136](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#136)]  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [IWorkerThreadClient Interface](../vs140/IWorkerThreadClient-Interface.md)   
 [CWorkerThread::AddHandle](../vs140/CWorkerThread--AddHandle.md)