---
title: "How to: Edit a Register Value"
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
ms.assetid: e27b6bd8-e6d4-4f1d-8a86-9f4047bb1167
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Edit a Register Value
The Registers window is available only if address-level debugging is enabled in the **Options** dialog box, **Debugging** node.  
  
### To change the value of a register  
  
1.  In the **Registers** window, use the TAB key or the mouse to move the insertion point to the value you want to change. When you start to type, the cursor must be located in front of the value you want to overwrite.  
  
2.  Type the new value.  
  
    > [!CAUTION]
    >  Changing register values (especially in the EIP and EBP registers) can affect program execution.  
  
    > [!CAUTION]
    >  Editing floating-point values can result in minor inaccuracies because of decimal-to-binary conversion of fractional components. Even a seemingly innocuous edit can result in changes to some of the least significant bits in a floating-point register.  
  
## See Also  
 [How to: Use the Registers Window](../vs140/How-to--Use-the-Registers-Window.md)