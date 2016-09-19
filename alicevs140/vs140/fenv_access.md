---
title: "fenv_access"
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
ms.assetid: 2ccea292-0ae4-42ce-9c67-cc189299857b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fenv_access
Disables (ON) or enables (OFF) optimizations that could change flag tests and mode changes.  
  
## Syntax  
  
```  
#pragma fenv_access [ON | OFF]  
```  
  
## Remarks  
 By default, `fenv_access` is OFF.  
  
 For more information on floating-point behavior, see [/fp (Specify Floating-Point Behavior)](../Topic/-fp%20\(Specify%20Floating-Point%20Behavior\).md).  
  
 The kinds of optimizations that are subject to `fenv_access` are:  
  
-   Global common subexpression elimination  
  
-   Code motion  
  
-   Constant folding  
  
 Other floating-point pragmas include:  
  
-   [float_control](../vs140/float_control.md)  
  
-   [fp_contract](../vs140/fp_contract.md)  
  
## Example  
  
```  
// pragma_directive_fenv_access_x86.cpp  
// compile with: /O2  
// processor: x86  
#include <stdio.h>  
#include <float.h>   
#include <errno.h>  
#pragma fenv_access (on)  
  
int main() {  
   double z, b = 0.1, t = 0.1;  
   unsigned int currentControl;  
   errno_t err;  
  
   err = _controlfp_s(&currentControl, _PC_24, _MCW_PC);  
   if (err != 0) {  
      printf_s("The function _controlfp_s failed!\n");  
      return -1;  
   }  
   z = b * t;  
   printf_s ("out=%.15e\n",z);  
}  
```  
  
 **out=9.999999776482582e-003**   
## Example  
 The following sample is for compiler producing output files for Itanium processors. **/fp:precise** keeps the intermediate results in extended precision where values greater than FLT_MAX (3.402823466e+38F) can be calculated and as a result of that sum will have 1.0 result, as it should if manually calculated. **/fp:strict** keeps intermediate results in their source precision (float) so the first addition produces infinity, which is kept throughout the expression.  
  
```  
// pragma_directive_fenv_access_IPF.cpp  
// compile with: /O2 /fp:precise  
// processor: IPF  
// compiling with /fp:precise prints 1.0F  
// compile with /fp:strict to print infinity  
  
#include <stdio.h>  
float arr[5] = {3.402823465e+38F,   
               3.402823462e+38F,  
               3.402823464e+38F,  
               3.402823463e+38F,  
               1.0F};  
  
int main() {  
   float sum = 0;  
   sum = arr[0] + arr[1] - arr[2] - arr[3] + arr[4];  
   printf_s("%f\n", sum);  
}  
```  
  
 **1.000000**   
## Example  
 When commenting out `#pragma fenv_access (on)` from the previous sample, note that the output is different because the compiler does compile-time evaluation, which does not use the control mode.  
  
```  
// pragma_directive_fenv_access_2.cpp  
// compile with: /O2  
#include <stdio.h>  
#include <float.h>   
  
int main() {  
   double z, b = 0.1, t = 0.1;  
   unsigned int currentControl;  
   errno_t err;  
  
   err = _controlfp_s(&currentControl, _PC_24, _MCW_PC);  
   if (err != 0) {  
      printf_s("The function _controlfp_s failed!\n");  
      return -1;  
   }  
   z = b * t;  
   printf_s ("out=%.15e\n",z);  
}  
```  
  
 **out=1.000000000000000e-002**   
## See Also  
 [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)