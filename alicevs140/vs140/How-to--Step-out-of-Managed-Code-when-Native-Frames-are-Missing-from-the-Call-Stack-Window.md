---
title: "How to: Step out of Managed Code when Native Frames are Missing from the Call Stack Window"
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
ms.assetid: 97cdd2a8-02a9-4a06-a5b1-c92b1e431979
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Step out of Managed Code when Native Frames are Missing from the Call Stack Window
If your code has native frames that are invisible in the **Call Stack** window, stepping out of managed code can produce unexpected results. As a workaround, you can use a breakpoint instead of **Step Out**.  
  
> [!NOTE]
>  The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition. To change your settings, choose **Import and Export Settings** on the **Tools** menu. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### To step out of managed code when native frames are missing from the call stack display  
  
1.  In the native code, set a location breakpoint after the call to managed code.  
  
2.  On the **Debug** menu, choose **Continue**.  
  
     When the managed call is completed, execution will stop at the breakpoint in native code.  
  
## See Also  
 [How to: Use the Call Stack Window](../vs140/How-to--Use-the-Call-Stack-Window.md)