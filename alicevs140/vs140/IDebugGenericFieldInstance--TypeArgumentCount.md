---
title: "IDebugGenericFieldInstance::TypeArgumentCount"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e662c5ea-a5c1-478e-a268-5980dadffcd1
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugGenericFieldInstance::TypeArgumentCount
Returns the number of type parameter arguments for this instance.  
  
## Syntax  
  
```cpp#  
HRESULT TypeArgumentCount(  
   ULONG32* pcArgs  
);  
```  
  
```c#  
int TypeArgumentCount(  
   ref uint pcArgs  
);  
```  
  
#### Parameters  
 `pcArgs`  
 [in, out] Number of type parameter arguments for this instance.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 For example, if List<int\>, this method returns 1, and, if List<int,float2> this method returns 2. This method returns 0 if there are no type arguments.  
  
## See Also  
 [IDebugGenericFieldInstance](../vs140/IDebugGenericFieldInstance.md)