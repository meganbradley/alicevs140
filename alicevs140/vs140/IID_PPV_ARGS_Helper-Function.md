---
title: "IID_PPV_ARGS_Helper Function"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: afee9b23-8df1-4575-903f-e9ba748418f0
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IID_PPV_ARGS_Helper Function
Verifies that the type of the specified argument derives from the `IUnknown` interface.  
  
> [!IMPORTANT]
>  This template specialization supports the WRL infrastructure and is not intended to be used directly from your code. Use [IID_PPV_ARGS](http://msdn.microsoft.com/library/windows/desktop/ee330727.aspx) instead.  
  
## Syntax  
  
```  
template<  
   typename T  
>  
void** IID_PPV_ARGS_Helper(  
   _Inout_ Microsoft::WRL::Details::ComPtrRef<T> pp  
);  
```  
  
#### Parameters  
 `T`  
 The type of argument `pp`.  
  
 `pp`  
 A doubly-indirect pointer.  
  
## Return Value  
 Argument `pp` cast to a pointer-to-a-pointer to `void`.  
  
## Remarks  
 A compile-time error is generated if the template parameter `T` doesn't derive from `IUnknown`.  
  
## Requirements  
 **Header:** client.h  
  
## See Also  
 [Reference (Windows Runtime Library)](assetId:///00000000-0000-0000-0000-000000000000)