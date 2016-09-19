---
title: "fp_contract"
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
ms.assetid: 15b97338-6680-4287-ba2a-2dccc5b2ccf5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fp_contract
Determines whether floating-point contraction will take place.  
  
## Syntax  
  
```  
#pragma fp_contract [ON | OFF]  
```  
  
## Remarks  
 By default, `fp_contract` is ON.  
  
 For more information on floating-point behavior, see [/fp (Specify Floating-Point Behavior)](../Topic/-fp%20\(Specify%20Floating-Point%20Behavior\).md).  
  
 Other floating-point pragmas include:  
  
-   [fenv_access](../vs140/fenv_access.md)  
  
-   [float_control](../vs140/float_control.md)  
  
## Example  
 The code generated from this sample does not use the Fused Multiply Add (**fma**) instruction on Itanium processors. If you comment out `#pragma fp_contract (off)`, the generated code will use the **fma** instruction.  
  
```  
// pragma_directive_fp_contract.cpp  
// compile with: /O2  
#include <stdio.h>  
#include <float.h>  
  
#pragma fp_contract (off)   
  
int main() {  
   double z, b, t;  
  
   for (int i = 0; i < 10; i++) {  
      b = i * 5.5;  
      t = i * 56.025;  
      _set_controlfp(_PC_24, _MCW_PC);  
  
      z = t * i + b;  
      printf_s ("out=%.15e\n", z);  
   }  
}  
```  
  
 **out=0.000000000000000e+000**  
**out=6.152500152587891e+001**  
**out=2.351000061035156e+002**  
**out=5.207249755859375e+002**  
**out=9.184000244140625e+002**  
**out=1.428125000000000e+003**  
**out=2.049899902343750e+003**  
**out=2.783724853515625e+003**  
**out=3.629600097656250e+003**  
**out=4.587524902343750e+003**   
## See Also  
 [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)