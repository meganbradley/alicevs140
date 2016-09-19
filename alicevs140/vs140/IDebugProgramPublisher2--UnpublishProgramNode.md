---
title: "IDebugProgramPublisher2::UnpublishProgramNode"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 57c7e6e1-b84e-4e14-ad83-cbbb64e2f526
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramPublisher2::UnpublishProgramNode
Removes a specified program node from availability to debug engines (DEs) and the session debug manager (SDM).  
  
## Syntax  
  
```cpp  
HRESULT UnpublishProgramNode(  
   IDebugProgramNode2* pProgramNode  
);  
```  
  
```c#  
int UnpublishProgramNode(  
   IDebugProgramNode2 pProgramNode  
);  
```  
  
#### Parameters  
 `pProgramNode`  
 [in] An [IDebugProgramNode2](../vs140/IDebugProgramNode2.md) object representing the program node being removed.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Once removed, the program node is no longer available to be queried for program information.  
  
 To make a program node available, call the [IDebugProgramPublisher2::PublishProgramNode](../vs140/IDebugProgramPublisher2--PublishProgramNode.md) method.  
  
## See Also  
 [IDebugProgramPublisher2](../vs140/IDebugProgramPublisher2.md)   
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)   
 [IDebugProgramPublisher2::PublishProgramNode](../vs140/IDebugProgramPublisher2--PublishProgramNode.md)