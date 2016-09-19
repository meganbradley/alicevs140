---
title: "IEnumDebugObjects::Clone"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cb7df109-d29a-4218-b900-6809091459dd
caps.latest.revision: 7
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugObjects::Clone
This method returns a copy of the current enumeration as a separate object.  
  
## Syntax  
  
```cpp#  
HRESULT Clone(  
   IEnumDebugObjects** ppEnum  
);  
```  
  
```c#  
int Clone(  
   out IEnumDebugObjects ppEnum  
);  
```  
  
#### Parameters  
 `ppEnum`  
 [out] Returns a copy of this enumeration as a separate object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The copy of the enumeration has the same state as the original at the time this method is called. However, the copy's and the original's states are separate and can be changed individually.  
  
## See Also  
 [IEnumDebugObjects](../vs140/IEnumDebugObjects.md)