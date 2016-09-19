---
title: "__getcallerseflags"
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
ms.assetid: 2386596f-33aa-4cc7-b026-5a834637270a
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __getcallerseflags
**Microsoft Specific**  
  
 Returns the EFLAGS value from the caller's context.  
  
## Syntax  
  
```  
unsigned int __getcallerseflags(void);  
```  
  
## Return Value  
 EFLAGS value from the caller's context.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__getcallerseflags`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 This routine is only available as an intrinsic.  
  
## Example  
  
```  
// getcallerseflags.cpp  
// processor: x86, x64  
  
#include <stdio.h>  
#include <intrin.h>  
  
#pragma intrinsic(__getcallerseflags)  
  
unsigned int g()  
{  
    unsigned int EFLAGS = __getcallerseflags();  
    printf_s("EFLAGS 0x%x\n", EFLAGS);  
    return EFLAGS;  
}  
unsigned int f()  
{  
    return g();  
}  
  
int main()  
{  
    unsigned int i;  
    i = f();  
    i = g();  
    return 0;  
}  
```  
  
 **EFLAGS 0x202**  
**EFLAGS 0x206**   
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)