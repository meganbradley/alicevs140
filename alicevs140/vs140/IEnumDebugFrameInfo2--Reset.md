---
title: "IEnumDebugFrameInfo2::Reset"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e149b559-f072-480b-9552-a452b147f3a8
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugFrameInfo2::Reset
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
 After this method is called, the next call to the [IEnumDebugFrameInfo2::Next](../vs140/IEnumDebugFrameInfo2--Next.md) method returns the first element of the enumeration.  
  
## See Also  
 [IEnumDebugFrameInfo2](../vs140/IEnumDebugFrameInfo2.md)