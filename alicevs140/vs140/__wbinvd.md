---
title: "__wbinvd"
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
ms.assetid: 628d0981-39e5-49e1-bd43-706d123af121
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __wbinvd
**Microsoft Specific**  
  
 Generates the Write Back and Invalidate Cache (`wbinvd`) instruction.  
  
## Syntax  
  
```  
void __wbinvd(void);  
```  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__wbinvd`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 This function is only available in kernel mode with a privilege level (CPL) of 0, and the routine is only available as an intrinsic.  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)