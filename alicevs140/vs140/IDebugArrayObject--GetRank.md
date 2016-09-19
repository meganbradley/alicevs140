---
title: "IDebugArrayObject::GetRank"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9948551a-e334-4ff6-979c-08dab633b9b6
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugArrayObject::GetRank
Gets the rank of the array, that is, the number of dimensions.  
  
## Syntax  
  
```cpp#  
HRESULT GetRank(   
   DWORD* pdwRank  
);  
```  
  
```c#  
int GetRank(  
   out uint pdwRank  
);  
```  
  
#### Parameters  
 `pdwRank`  
 [out] Returns the rank.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 Use the [IDebugArrayObject::GetDimensions](../vs140/IDebugArrayObject--GetDimensions.md) method to retrieve the size of each dimension of the array object.  
  
## See Also  
 [IDebugArrayObject](../vs140/IDebugArrayObject.md)