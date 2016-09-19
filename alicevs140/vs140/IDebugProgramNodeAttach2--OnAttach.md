---
title: "IDebugProgramNodeAttach2::OnAttach"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5fe52761-a508-4ab5-abdb-334fb6590334
caps.latest.revision: 5
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramNodeAttach2::OnAttach
Attaches to the associated program or defers the attach process to the [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md) method.  
  
## Syntax  
  
```cpp#  
HRESULT OnAttach(  
   [in] REFGUID guidProgramId  
);  
```  
  
```c#  
int OnAttach(  
   ref Guid guidProgramId  
};  
```  
  
#### Parameters  
 `guidProgramId`  
 [in] `GUID` to assign to the associated program.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if the [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md) method should not be called. Otherwise, returns an error code.  
  
## Remarks  
 This method is called during the attach process, before the [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md) method is called. The `OnAttach` method can perform the attach process itself (in which case, this method returns `S_FALSE`) or defer the attach process to the `IDebugEngine2::Attach` method (the `OnAttach` method returns `S_OK`). In either event, the `OnAttach` method can set the `GUID` of the program being debugged to the given `GUID`.  
  
## See Also  
 [IDebugProgramNodeAttach2](../vs140/IDebugProgramNodeAttach2.md)   
 [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md)