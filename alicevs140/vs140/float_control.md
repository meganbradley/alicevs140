---
title: "float_control"
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
ms.assetid: 4f4ba5cf-3707-413e-927d-5ecdbc0a9a43
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# float_control
Specifies floating-point behavior for a function.  
  
## Syntax  
  
```  
float_control( value,setting [push] | push | pop )  
```  
  
## Flags  
 `value` *,* `setting` **[push]**  
 Specifies floating-point behavior. `value` can be **precise** or **except**. For more information, see [/fp (Specify Floating-Point Behavior)](../Topic/-fp%20\(Specify%20Floating-Point%20Behavior\).md). `setting` can either be **on** or **off**.  
  
 If `value` is **precise**, the settings for **precise** and **except** are being specified. **except** can only be set to **on** when **precise** is also set to **on**.  
  
 If the optional **push** token is added, the current setting for `value` is pushed on to the internal compiler stack.  
  
 **push**  
 Push the current `float_control` setting on to the internal compiler stack  
  
 **pop**  
 Removes the`float_control` setting from the top of the internal compiler stack and makes that the new `float_control` setting.  
  
## Remarks  
 You cannot turn `float_control precise` off when **except** is on. Similarly, **precise** cannot be turned off when `fenv_access` is on. To go from strict model to a fast model with the `float_control` pragma, use the following code:  
  
```  
#pragma float_control(except, off)  
#pragma fenv_access(off)  
#pragma float_control(precise, off)  
// The following line is needed on Itanium processors  
#pragma fp_contract(on)  
```  
  
 To go from fast model to a strict model with the `float_control` pragma, use the following code:  
  
```  
#pragma float_control(precise, on)  
#pragma fenv_access(on)  
#pragma float_control(except, on)  
// The following line is needed on Itanium processors.  
#pragma fp_contract(off)  
```  
  
 Other floating-point pragmas include:  
  
-   [fenv_access](../vs140/fenv_access.md)  
  
-   [fp_contract](../vs140/fp_contract.md)  
  
## Example  
 The following sample shows how to catch an overflow floating-point exception by using pragma `float_control`.  
  
```  
// pragma_directive_float_control.cpp  
// compile with: /EHa  
#include <stdio.h>  
#include <float.h>  
  
double func( ) {  
   return 1.1e75;  
}  
  
#pragma float_control (except,on)  
  
int main( ) {  
   float u[1];  
   unsigned int currentControl;  
   errno_t err;  
  
   err = _controlfp_s(&currentControl, ~_EM_OVERFLOW, _MCW_EM);  
   if (err != 0)  
      printf_s("_controlfp_s failed!\n");  
  
   try  {  
      u[0] = func();  
      printf_s ("Fail");     
      return(1);  
   }   
  
   catch (...)  {  
      printf_s ("Pass");  
      return(0);  
   }  
}  
```  
  
 **Pass**   
## See Also  
 [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)