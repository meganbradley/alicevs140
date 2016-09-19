---
title: "How to: Debug Injected Code"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a1b4104d-d49e-451f-a91e-e39ceaf35875
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Debug Injected Code
> [!NOTE]
>  The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition. To change your settings, choose Import and Export Settings on the Tools menu. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
 Using attributes can greatly simplify C++ programming. For more information, see [Attributed Programming Concepts](../vs140/Attributed-Programming-Concepts.md). Some attributes are interpreted directly by the compiler. Other attributes inject code into the program source, which the compiler then compiles. This injected code makes programming easier by reducing the amount of code you have to write. Sometimes, however, a bug may cause your application to fail while it is executing injected code. When this happens, you will probably want to look at the injected code. Visual Studio provides two ways for you to see injected code:  
  
-   You can view injected code in the **Disassembly** window.  
  
-   Using [/Fx](../vs140/-Fx--Merge-Injected-Code-.md), you can create a merged source file that contains original and injected code.  
  
 The **Disassembly** window shows assembly-language instructions that correspond to the source code and the code injected by attributes. In addition, the **Disassembly** window can show the source-code annotation.  
  
### To turn on Source Annotation  
  
-   Right-click the **Disassembly** window, and choose **Show Source Code** from the shortcut menu.  
  
     If you know the location of an attribute in a source window, you can use the shortcut menu to find the injected code in the **Disassembly** window.  
  
### To view injected code  
  
1.  The debugger must be in break mode.  
  
2.  In a source code window, place the cursor in front of the attribute whose injected code you want to view.  
  
3.  Right-click, and select **Go To Disassembly** from the shortcut menu.  
  
     If the attribute location is near the current execution point, you can select the **Disassembly** window from the **Debug** menu.  
  
### To view the disassembly code at the current execution point  
  
1.  The debugger must be in break mode.  
  
2.  From the **Debug** menu, choose **Windows**, and click **Disassembly**.  
  
## See Also  
 [Debugger Security](../vs140/Debugger-Security.md)   
 [Debugging Native Code](../vs140/Debugging-Native-Code.md)