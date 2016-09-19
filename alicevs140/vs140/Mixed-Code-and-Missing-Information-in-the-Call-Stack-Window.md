---
title: "Mixed Code and Missing Information in the Call Stack Window"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - JScript
  - SQL
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
ms.assetid: dd628427-e8d6-4fc2-b524-9d6393ea5376
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mixed Code and Missing Information in the Call Stack Window
Because of differences between call stacks for managed and native code, the debugger cannot always show the complete call stack when the code types mix. When native code calls managed code, you may notice the following discrepancies in the **Call Stack** window:  
  
-   The native frame immediately above the managed code may be missing from the **Call Stack** window. For more information, see [How to: Step out of Managed Code when Native Frames are Missing from the Call Stack Window](../vs140/How-to--Step-out-of-Managed-Code-when-Native-Frames-are-Missing-from-the-Call-Stack-Window.md).  
  
-   For mixed-mode applications launched outside the debugger, the **Call Stack** window may display only the managed code and none of the native frames will be visible.  
  
 Both cases are fairly rare. In most native calls to managed code, call stacks appear correctly.  
  
## See Also  
 [How to: Use the Call Stack Window](../vs140/How-to--Use-the-Call-Stack-Window.md)