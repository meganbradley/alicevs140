---
title: "__readeflags"
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
ms.assetid: f9d2f4d8-c428-491f-b8de-04d0566b2b6b
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __readeflags
Reads the program status and control (EFLAGS) register.  
  
## Syntax  
  
```  
unsigned     int __readeflags(void);  
unsigned __int64 __readeflags(void);  
```  
  
## Return Value  
 The value of the EFLAGS register. The return value is 32 bits long on a 32-bit platform and 64 bits long on a 64-bit platform.  
  
## Remarks  
 These routines are available only as intrinsics.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__readeflags`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [__writeeflags](../vs140/__writeeflags.md)