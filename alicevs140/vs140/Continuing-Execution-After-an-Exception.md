---
title: "Continuing Execution After an Exception"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - JScript
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
ms.assetid: 6fe97aac-2131-4615-bd92-d3afee741558
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Continuing Execution After an Exception
When the debugger breaks execution because of an exception, a dialog box appears. For Visual Basic or C#, you will see the [Exception Assistant](../vs140/Exception-Assistant.md) dialog box, by default. For C++, you will see the older **Exception** dialog box. If you are using Visual Basic or C# but have disabled the **Exception Assistant** in the **Options** dialog box, you will see the **Exception** dialog box.  
  
 When the **Exception Assistant** or **Exception** dialog box appears, you can try to fix the problem that caused the exception.  
  
## Managed Code  
 In managed code, you can continue execution in the same thread after an unhandled exception. The **Exception Assistant** unwinds the call stack to the point where the exception was thrown.  
  
## Native Code  
 In native C/C++, you have two options:  
  
-   You can click **Break** and try to fix the problem. While you are in Break mode, you can unwind the call stack by right-clicking on a frame in the **Call Stack** window and selecting **Unwind to this Frame** on the shortcut menu. When you continue to debug, the **Exception** dialog box appears again if you have not fixed the problem. Otherwise, the **Exception** dialog box will not reappear.  
  
-   You can click **Continue** to continue execution without trying to fix the problem. The **Exception** dialog box reappears.  
  
## Mixed Code  
 If you hit an unhandled exception while debugging a mixed native and managed code, operating system constraints prevent unwinding the call stack. If you try rewinding the call stack using the shortcut menu, an error message explains that the debugger cannot unwind from an unhandled except during mixed-code debugging.  
  
## See Also  
 [Managing Exceptions with the Debugger](../Topic/Managing%20Exceptions%20with%20the%20Debugger.md)