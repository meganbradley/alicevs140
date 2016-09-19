---
title: "IEnumDebugPrograms2::Reset"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b289242b-24ea-4df3-a811-20b0c8a903d6
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugPrograms2::Reset
Resets the enumeration to the first element.  
  
## Syntax  
  
```cpp#  
HRESULT Reset(  
   void  
);  
```  
  
```c#  
int Reset();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 After this method is called, the next call to the [IEnumDebugPrograms2::Next](../vs140/IEnumDebugPrograms2--Next.md) method returns the first element of the enumeration.  
  
## See Also  
 [IEnumDebugPrograms2](../vs140/IEnumDebugPrograms2.md)