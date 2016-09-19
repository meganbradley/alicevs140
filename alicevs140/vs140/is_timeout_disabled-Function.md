---
title: "is_timeout_disabled Function"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 280bd439-48f1-4c17-8c29-1c98774d1930
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# is_timeout_disabled Function
Returns a boolean flag indicating if timeout is disabled for the specified accelerator_view. This corresponds to the D3D11_CREATE_DEVICE_DISABLE_GPU_TIMEOUT flag for Direct3D device creation.  
  
## Syntax  
  
```  
bool __cdecl is_timeout_disabled(  
   const accelerator_view& _Accelerator_view  
);  
```  
  
#### Parameters  
 `_Accelerator_view`  
 The accelerator_view for which the timeout disabled setting is to be queried.  
  
## Return Value  
 A boolean flag indicating if timeout is disabled for the specified accelerator_view.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** concurrency::direct3d  
  
## See Also  
 [concurrency::direct3d Namespace](../vs140/Concurrency--direct3d-Namespace.md)