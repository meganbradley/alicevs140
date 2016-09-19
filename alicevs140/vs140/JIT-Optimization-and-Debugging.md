---
title: "JIT Optimization and Debugging"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 19bfabf3-1a2e-49dc-8819-a813982e86fd
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# JIT Optimization and Debugging
When you debug a managed application, [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] suppresses optimization of just-in-time (JIT) code by default. Suppressing JIT optimization means you are debugging non-optimized code. The code runs a bit slower because it is not optimized, but your debugging experience is much more thorough. Debugging optimized code is harder and recommended only if you encounter a bug that occurs in optimized code but cannot be reproduced in the non-optimized version.  
  
 JIT optimization is controlled in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] by the **Suppress JIT optimization on module load** option. You can find this option on the **General** page under the **Debugging** node in the **Options** dialog box.  
  
 If you clear the **Suppress JIT optimization on module load** option, you can debug optimized JIT code, but your ability to debug may be limited because the optimized code does not match the source code. As a result, debugger windows such as the **Locals** and **Autos** window may not display as much information as they would if you were debugging non-optimized code.  
  
 Another important difference concerns debugging with Just My Code. If you are debugging with Just My Code, the debugger considers optimized code to be non-user code, which should not be displayed while you are debugging. Consequently, if you are debugging JIT optimized code, you probably want to turn Just My Code off. For more information, see  [Restrict stepping to Just My Code](../vs140/Navigating-through-Code-with-the-Debugger.md#BKMK_Restrict_stepping_to_Just_My_Code).  
  
 Remember that the **Suppress JIT optimization on module load** option suppresses optimization of code when modules are loaded. If you attach to a process that is already running, it may contain code that is already loaded, JIT-compiled, and optimized. The **Suppress JIT optimization on module load** option has no effect on such code, although it will affect modules that are loaded after you attach. In addition, the **Suppress JIT optimization on module load** option does not affect modules, such as WinForms.dll, that are created with NGEN.  
  
## See Also  
 [Debugging Managed Code](../Topic/Debugging%20Managed%20Code.md)   
 [Start, Break, Step, Run through Code, and Stop Debugging in Visual Studio](../vs140/Navigating-through-Code-with-the-Debugger.md)   
 [Attaching to Running Processes](../vs140/Attach-to-Running-Processes-with-the-Visual-Studio-Debugger.md)   
 [Managed Execution Process](assetId:///476b03dc-2b12-49a7-b067-41caeaa2f533)