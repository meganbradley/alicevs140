---
title: "__readmsr"
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
ms.assetid: 7ab1f8e8-72cb-4ce4-817d-3e728a3c9716
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __readmsr
**Microsoft Specific**  
  
 Generates the `rdmsr` instruction, which reads the model-specific register specified by `register` and returns its value.  
  
## Syntax  
  
```  
__int64 __readmsr(   
   int register   
);  
```  
  
#### Parameters  
 [in] `register`  
 The model specific register to read.  
  
## Return Value  
 The value in the specified register.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__readmsr`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 This function is only available in kernel mode, and the routine is only available as an intrinsic.  
  
 For more information, see the AMD documentation.  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)