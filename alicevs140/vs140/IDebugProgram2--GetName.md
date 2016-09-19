---
title: "IDebugProgram2::GetName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a54cbf13-b3e3-4c9f-8b8d-13573232dfb0
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram2::GetName
Gets the name of the program.  
  
## Syntax  
  
```cpp#  
HRESULT GetName(   
   BSTR* pbstrName  
);  
```  
  
```c#  
int GetName(   
   out string pbstrName  
);  
```  
  
#### Parameters  
 `pbstrName`  
 [out] Returns the name of the program.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The name returned by this method is always a friendly, user-displayable name that describes the program.  
  
## See Also  
 [IDebugProgram2](../vs140/IDebugProgram2.md)