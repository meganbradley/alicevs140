---
title: "IEnumDebugObjects::Reset"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4a245e47-cc39-4177-b83d-083ea0e3190f
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugObjects::Reset
This method resets the enumeration to the first element.  
  
## Syntax  
  
```cpp#  
HRESULT Reset(void);  
```  
  
```c#  
int Reset();  
```  
  
#### Parameters  
 None  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 After this method is called, the next call to [IEnumDebugObjects::Next](../vs140/IEnumDebugObjects--Next.md) returns the first element of the enumeration.  
  
## See Also  
 [IEnumDebugObjects](../vs140/IEnumDebugObjects.md)   
 [IEnumDebugObjects::Next](../vs140/IEnumDebugObjects--Next.md)