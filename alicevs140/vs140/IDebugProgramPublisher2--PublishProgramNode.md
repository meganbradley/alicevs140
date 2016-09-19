---
title: "IDebugProgramPublisher2::PublishProgramNode"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d4b72e04-f726-46cf-8e56-5203ff205b12
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramPublisher2::PublishProgramNode
Makes a program node available for use by debug engines (DEs) and the session debug manager (SDM).  
  
## Syntax  
  
```cpp  
HRESULT PublishProgramNode(  
   IDebugProgramNode2 *pProgramNode  
);  
```  
  
```c#  
int PublishProgramNode(  
   IDebugProgramNode2 pProgramNode  
);  
```  
  
#### Parameters  
 `pProgramNode`  
 [in] An [IDebugProgramNode2](../vs140/IDebugProgramNode2.md) object that represents the program node to make available.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method allows programs to be queried for information before selecting and launching them for debugging.  
  
 To remove a program node from availability, call the [IDebugProgramPublisher2::UnpublishProgramNode](../vs140/IDebugProgramPublisher2--UnpublishProgramNode.md) method.  
  
## See Also  
 [IDebugProgramPublisher2](../vs140/IDebugProgramPublisher2.md)   
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)   
 [IDebugProgramPublisher2::UnpublishProgramNode](../vs140/IDebugProgramPublisher2--UnpublishProgramNode.md)