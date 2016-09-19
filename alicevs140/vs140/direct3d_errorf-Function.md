---
title: "direct3d_errorf Function"
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
ms.assetid: a4098d87-6dec-416a-b271-21f2f19d44fd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# direct3d_errorf Function
Prints a formatted string to the Visual Studio output window. It is called from a function with the `restrict(amp)` restriction clause. When the AMP runtime detects the call, it raises a [runtime_exception](../vs140/runtime_exception-Class.md) exception with the same formatting string.  
  
## Syntax  
  
```  
void direct3d_errorf(  
   const char *,  
   ...  
) restrict(amp);  
```  
  
## Remarks  
 This function has the following restrictions:  
  
1.  The Debug configuration in Visual Studio is selected, i.e. the code is compiled with the _DEBUG preprocessor definition.  
  
2.  The [accelerator_view](assetId:///accelerator_view?qualifyHint=False&autoUpgrade=True) on which the kernel is invoked must be on an accelerator which supports the printf, errorf, and abort intrinsics. These are supported by the REF accelerator. For more information, see [Using accelerator and accelerator_view Objects](../vs140/Using-accelerator-and-accelerator_view-Objects.md).  
  
3.  The maximum number of parameters allowed is seven.  
  
4.  There is no automatic widening or narrowing type conversion.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [Concurrency Namespace (C++ AMP)](../vs140/Concurrency-Namespace--C---AMP-.md)