---
title: "IDebugProgramEx2::GetProgramNode"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1545ffbf-1422-4b5d-9bb9-314ba8665041
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramEx2::GetProgramNode
Gets the program node associated with a program.  
  
## Syntax  
  
```cpp#  
HRESULT GetProgramNode(   
   IDebugProgramNode2** ppProgramNode  
);  
```  
  
```c#  
int GetProgramNode(   
   out IDebugProgramNode2 ppProgramNode  
);  
```  
  
#### Parameters  
 `ppProgramNode`  
 [out] Returns an [IDebugProgramNode2](../vs140/IDebugProgramNode2.md) object that represents the program node associated with this program.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugProgramEx2](../vs140/IDebugProgramEx2.md)   
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)