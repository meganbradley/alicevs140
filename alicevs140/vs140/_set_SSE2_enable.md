---
title: "_set_SSE2_enable"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _set_SSE2_enable
apilocation: 
  - msvcr80.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 55db895d-fc1e-475a-9110-b781a9bb51c5
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _set_SSE2_enable
Enables or disables the use of [Streaming SIMD Extensions 2](assetId:///f98440eb-73a9-4f96-b203-ac41bb6701ea) (SSE2) instructions in CRT math routines. (This function is not available on x64 architectures because SSE2 is enabled by default.)  
  
## Syntax  
  
```  
int _set_SSE2_enable(  
   int flag  
);  
```  
  
#### Parameters  
 `flag`  
 1 to enable the SSE2 implementation; 0 to disable the SSE2 implementation. By default, SSE2 implementation is enabled on processors that support it.  
  
## Return Value  
 Nonzero if SSE2 implementation is enabled; zero if SSE2 implementation is disabled.  
  
## Remarks  
 The following functions have SSE2 implementations that can be enabled by using `_set_SSE2_enable`:  
  
-   [atan](../vs140/atan--atanf--atanl--atan2--atan2f--atan2l.md)  
  
-   [ceil](../vs140/ceil--ceilf--ceill.md)  
  
-   [exp](../vs140/exp--expf.md)  
  
-   [floor](../vs140/floor--floorf--floorl.md)  
  
-   [log](../vs140/log--logf--log10--log10f.md)  
  
-   [log10](../vs140/log--logf--log10--log10f.md)  
  
-   [modf](../vs140/modf--modff--modfl.md)  
  
-   [pow](../vs140/pow--powf--powl.md)  
  
 The SSE2 implementations of these functions might give slightly different answers than the default implementations, because SSE2 intermediate values are 64-bit floating-point quantities but the default implementation intermediate values are 80-bit floating-point quantities.  
  
> [!NOTE]
>  If you use the [/Oi (Generate Intrinsic Functions)](../vs140/-Oi--Generate-Intrinsic-Functions-.md) compiler option to compile the project, it may appear that `_set_SSE2_enable` has no effect. The `/Oi` compiler option gives the compiler the authority to use intrinsics to replace CRT calls; this behavior overrides the effect of `_set_SSE2_enable`. If you want to guarantee that `/Oi` does not override `_set_SSE2_enable`, use `/Oi-` to compile your project. This might also be good practice when you use other compiler switches that imply `/Oi`.  
  
 The SSE2 implementation is only used if all exceptions are masked. Use [_control87, _controlfp](../vs140/_control87--_controlfp--__control87_2.md) to mask exceptions.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_set_SSE2_enable`|<math.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_set_SSE2_enable.c  
// processor: x86  
#include <math.h>  
#include <stdio.h>  
  
int main()  
{  
   int i = _set_SSE2_enable(1);  
  
   if (i)  
      printf("SSE2 enabled.\n");  
   else  
      printf("SSE2 not enabled; processor does not support SSE2.\n");  
}  
```  
  
 **Output**  
  
 `SSE2 enabled.`  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [CRT Library Features](../vs140/CRT-Library-Features.md)