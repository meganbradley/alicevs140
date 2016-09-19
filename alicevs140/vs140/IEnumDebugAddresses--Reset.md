---
title: "IEnumDebugAddresses::Reset"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a9d7f20-5bc6-4e13-8e91-5af4092e092f
caps.latest.revision: 7
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugAddresses::Reset
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
 After this method is called, the next call to [IEnumDebugAddresses::Next](../vs140/IEnumDebugAddresses--Next.md) returns the first element of the enumeration.  
  
## See Also  
 [IEnumDebugAddresses](../vs140/IEnumDebugAddresses.md)   
 [IEnumDebugAddresses::Next](../vs140/IEnumDebugAddresses--Next.md)