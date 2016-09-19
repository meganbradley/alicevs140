---
title: "RuntimeClass::GetRuntimeClassName Method"
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
ms.topic: reference
ms.assetid: f6388163-fe65-4948-a4bc-ae6826f480e7
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RuntimeClass::GetRuntimeClassName Method
Gets the runtime class name of the current RuntimeClass object.  
  
## Syntax  
  
```  
STDMETHOD(  
   GetRuntimeClassName  
)(_Out_ HSTRING* runtimeName);  
```  
  
## Parameters  
 `runtimeName`  
 When this operation completes, the runtime class name.  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that indicates the error.  
  
## Remarks  
 An assert error is emitted if __WRL_STRICT\__or \__WRL_FORCE_INSPECTABLE_CLASS_MACRO\_\_ isn't defined.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [RuntimeClass Class](../vs140/RuntimeClass-Class.md)