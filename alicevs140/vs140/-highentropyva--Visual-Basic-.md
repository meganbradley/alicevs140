---
title: "-highentropyva (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
H1: /highentropyva (Visual Basic)
ms.assetid: ff25f20a-6ca2-467b-9e52-5cf439f5028e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -highentropyva (Visual Basic)
Indicates whether a 64-bit executable or an executable that's marked by the [/platform:anycpu](../Topic/-platform%20\(Visual%20Basic\).md) compiler option supports high entropy Address Space Layout Randomization (ASLR).  
  
## Syntax  
  
```  
/highentropyva[+ | -]  
```  
  
## Arguments  
 `+` &#124; `-`  
 Optional. The option is off by default or if you specify `/highentropyva-`. The option is on if you specify `/highentropyva` or `/highentropyva+`.  
  
## Remarks  
 If you specify this option, compatible versions of the Windows kernel can use higher degrees of entropy when the kernel randomizes the address space layout of a process as part of ASLR. If the kernel uses higher degrees of entropy, a larger number of addresses can be allocated to memory regions such as stacks and heaps. As a result, it is more difficult to guess the location of a particular memory region.  
  
 When the option is on, the target executable and any modules on which it depends must be able to handle pointer values that are larger than 4 gigabytes (GB) when those modules are running as 64-bit processes.  
  
 For more information about ASLR, see [Mitigating Software Vulnerabilities](http://go.microsoft.com/fwlink/?LinkId=226234).  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)