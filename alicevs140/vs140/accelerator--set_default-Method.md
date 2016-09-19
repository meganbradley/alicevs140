---
title: "accelerator::set_default Method"
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
ms.assetid: 9863e4b2-35b4-4b14-b40c-917dd266605b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accelerator::set_default Method
Sets the default accelerator to be used for any operation that implicitly uses the default accelerator. This method only succeeds if the runtime selected default accelerator has not already been used in an operation that implicitly uses the default accelerator  
  
## Syntax  
  
```  
static inline bool set_default(  
   std::wstring _Path  
);  
```  
  
#### Parameters  
 `_Path`  
 The path to the accelerator.  
  
## Return Value  
 `true` if the call succeeds at setting the default accelerator. Otherwise, `false`.  
  
## Remarks  
 The C++ AMP runtime picks a default accelerator, unless you write code to pick a specific accelerator. For more information, see [Using accelerator and accelerator_view objects](../vs140/Using-accelerator-and-accelerator_view-Objects.md).  
  
 You can specify the default accelerator object in these ways:  
  
1.  Call the constructor that takes a device path parameter.  
  
2.  Set the default accelerator using the [accelerator::set_default Method](../vs140/accelerator--set_default-Method.md) and pass the value of [accelerator::default_accelerator Data Member](../vs140/accelerator--default_accelerator-Data-Member.md) to the constructor.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [accelerator Class](../vs140/accelerator-Class.md)   
 [Using accelerator and accelerator_view objects](../vs140/Using-accelerator-and-accelerator_view-Objects.md)