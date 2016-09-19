---
title: "IDebugFunctionPosition2::GetOffset"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 60943782-aec7-4be2-b222-1984ed53a543
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugFunctionPosition2::GetOffset
Retrieves the position of the function in the source document.  
  
## Syntax  
  
```cpp#  
HRESULT GetOffset(   
   TEXT_POSITION* pPosition  
);  
```  
  
```c#  
int GetOffset(  
   TEXT_POSITION[] pPosition  
);  
```  
  
#### Parameters  
 `pPosition`  
 [in, out] A [TEXT_POSITION](../vs140/TEXT_POSITION.md) structure that is filled in with the position of the function in a document.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugFunctionPosition2](../vs140/IDebugFunctionPosition2.md)   
 [TEXT_POSITION](../vs140/TEXT_POSITION.md)