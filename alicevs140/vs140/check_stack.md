---
title: "check_stack"
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
ms.assetid: f18e20cc-9abb-48b7-ad62-8d384875b996
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# check_stack
Instructs the compiler to turn off stack probes if **off** (or **–**) is specified, or to turn on stack probes if **on** (or **+**) is specified.  
  
## Syntax  
  
```  
  
      #pragma check_stack([ {on | off}] )  
#pragma check_stack{+ | –}  
```  
  
## Remarks  
 If no argument is given, stack probes are treated according to the default. This pragma takes effect at the first function defined after the pragma is seen. Stack probes are neither a part of macros nor of functions that are generated inline.  
  
 If you don't give an argument for the **check_stack** pragma, stack checking reverts to the behavior specified on the command line. For more information, see [Compiler Reference](../vs140/Compiler-Options.md). The interaction of the **#pragma check_stack** and the [/Gs](../vs140/-Gs--Control-Stack-Checking-Calls-.md) option is summarized in the following table.  
  
### Using the check_stack Pragma  
  
|Syntax|Compiled with<br /><br /> /Gs option?|Action|  
|------------|------------------------------------|------------|  
|**#pragma check_stack( )** or<br /><br /> **#pragma check_stack**|Yes|Turns off stack checking for functions that follow|  
|**#pragma check_stack( )** or<br /><br /> **#pragma check_stack**|No|Turns on stack checking for functions that follow|  
|**#pragma check_stack(on)**<br /><br /> or **#pragma check_stack +**|Yes or No|Turns on stack checking for functions that follow|  
|**#pragma check_stack(off)**<br /><br /> or **#pragma check_stack –**|Yes or No|Turns off stack checking for functions that follow|  
  
## See Also  
 [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)