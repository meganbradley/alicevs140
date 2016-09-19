---
title: "IDebugBinder3::GetTypeArgumentCount"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: caf68de6-6f7c-4efd-b803-121347a5032e
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBinder3::GetTypeArgumentCount
This method returns the number of argument types associated with this object.  
  
## Syntax  
  
```cpp  
HRESULT GetTypeArgumentCount(  
   UINT* uCount  
);  
```  
  
```c#  
int GetTypeArgumentCount(  
   out uint uCount  
);  
```  
  
#### Parameters  
 `uCount`  
 [out] Number of argument types associated with this object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The value returned by this method can be used to allocate an array for use with the [IDebugBinder3::GetTypeArguments](../vs140/IDebugBinder3--GetTypeArguments.md) method.  
  
## See Also  
 [IDebugBinder3](../vs140/IDebugBinder3.md)   
 [IDebugBinder3::GetTypeArguments](../vs140/IDebugBinder3--GetTypeArguments.md)