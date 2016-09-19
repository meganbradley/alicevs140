---
title: "Diagnostic Messages in the Output Window"
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
ms.assetid: 386e9524-be17-4573-83fb-4f7c5cae0be0
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Diagnostic Messages in the Output Window
You can write run-time messages to the Output window using the Debug class or the Trace class, which are part of the <xref:System.Diagnostics?qualifyHint=False> class library. Use the Debug class if you only output in the Debug version of your program. Use the Trace class if you want output in both the Debug and Release versions.  
  
## Output Methods  
 The <xref:System.Diagnostics.Trace?qualifyHint=False> and <xref:System.Diagnostics.Debug?qualifyHint=False> classes provide the following output methods:  
  
-   Various `Write` methods, which output information without breaking execution. These methods replace the `Debug.Print` method used in previous versions of Visual Basic.  
  
-   <xref:System.Diagnostics.Debug.Assert?qualifyHint=True> and <xref:System.Diagnostics.Trace.Assert?qualifyHint=True> methods, which break execution and outputs information if a specified condition fails. By default, the `Assert` method displays the information in a dialog box. For more information, see [Assertions in Managed Code](../Topic/Assertions%20in%20Managed%20Code.md).  
  
-   The <xref:System.Diagnostics.Debug.Fail?qualifyHint=True> and <xref:System.Diagnostics.Trace.Fail?qualifyHint=True> methods, which always breaks execution and outputs information. By default, the `Fail` methods display the information in a dialog box.  
  
 In addition to program out from your application, the **Output** window can display the information about:  
  
-   Modules the debugger has loaded or unloaded.  
  
-   Exceptions that are thrown.  
  
-   Processes that exit.  
  
-   Threads that exit.  
  
## See Also  
 [Debugger Security](../vs140/Debugger-Security.md)   
 [Output Window](../Topic/Output%20Window.md)   
 [Instrumentation Techniques (Debug and Trace) for the .NET Framework](assetId:///773b6fc4-9013-4322-b728-5dec7a72e743)   
 [Introduction to Instrumentation and Tracing](assetId:///e924e57c-33cf-4b0e-9e7f-a45d13e38f2c)   
 [C#, F#, and Visual Basic Project Types](../vs140/Debugging-Preparation--C#--F#--and-Visual-Basic-Project-Types.md)   
 [Debugging Managed Code](../Topic/Debugging%20Managed%20Code.md)