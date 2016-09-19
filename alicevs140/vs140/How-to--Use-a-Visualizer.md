---
title: "How to: Use a Visualizer"
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
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d2611385-0134-4387-8c5a-979fe625a462
caps.latest.revision: 39
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use a Visualizer
You can use a visualizer to display the contents of a variable or object in a way that is meaningful for the data type. You can use visualizers from **DataTips**, a **Watch** window, the **Autos** window, or the **Locals** window.  
  
 Visualizers are not supported on the Compact Framework.  
  
> [!NOTE]
>  In **Store** apps, only the standard text, HTML, XML, and JSON visualizers are supported. Custom (user-created) visualizers are not supported.  
  
### To open a visualizer  
  
1.  Click the magnifying glass icon that appears next to a variable name in **DataTips**, a **Watch** window, or in the **Autos**, **Locals**, or **Quick Watch** window.  
  
     A list of visualizers is displayed.  
  
2.  Click the visualizer you want to use.  
  
### To use a visualizer for managed code during remote debugging  
  
-   Copy the visualizer DLL to the remote computer before you start the debugging session.  
  
     The path to the DLL must be the same on both the remote and the local computers. This path can be either of the following locations:  
  
     *Visual Studio install path* `\Common7\Packages\Debugger\Visualizers`  
  
     -or-  
  
     `My Documents\Visual Studio 2010\Visualizers` *Visual Studio Version* `\Visualizers`  
  
## See Also  
 [Visualizers](../vs140/Create-Custom-Visualizers-of-Data.md)   
 [How to: Install a Visualizer](../vs140/How-to--Install-a-Visualizer.md)   
 [How to: Write a Visualizer](../Topic/How%20to:%20Write%20a%20Visualizer.md)   
 [How to: Use DataTips](../vs140/View-data-values-in-Data-Tips--in-the-code-editor.md)