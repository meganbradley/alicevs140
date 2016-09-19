---
title: "IDebugModule3::IsUserCode"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 77022946-bb8b-4114-aa81-614df6e54b13
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugModule3::IsUserCode
Retrieves information on whether the module represents user code or not.  
  
## Syntax  
  
```cpp#  
HRESULT IsUserCode(  
   BOOL* pfUser  
);  
```  
  
```c#  
int IsUserCode(  
   out int pfUser  
);  
```  
  
#### Parameters  
 `pfUser`  
 [out] Nonzero (`TRUE`) if module represents user code, zero (`FALSE`) if it does not.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## See Also  
 [IDebugModule3](../vs140/IDebugModule3.md)