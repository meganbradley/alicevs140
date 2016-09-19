---
title: "How Can I Find Out Who Is Passing a Wrong Parameter Value?"
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
ms.assetid: 1f1ae455-0e25-4e9d-b33f-53908f5bd6ce
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How Can I Find Out Who Is Passing a Wrong Parameter Value?
## Problem Description  
 The wrong parameter value is being passed to one of my functions. This function is called from all over the place. How can I find out what is passing it the wrong value?  
  
## Solution  
  
#### To resolve this problem  
  
1.  Set a location breakpoint at the beginning of the function.  
  
2.  Right-click the breakpoint and select **Condition**.  
  
3.  In the **Breakpoint Condition** dialog box, click on the **Condition** check box. See [Specify a breakpoint condition using a code expression](../vs140/Using-Breakpoints.md#BKMK_Specify_a_breakpoint_condition_using_a_code_expression).  
  
4.  Enter an expression, such as `Var==3`, into the text box, where `Var` is the name of the parameter that contains the bad value, and `3` is the bad value passed to it.  
  
5.  Select the **is True** radio button, and click the **OK** button.  
  
6.  Now run the program again. The breakpoint causes the program to halt at the beginning of the function when the `Var` parameter has the value `3`.  
  
7.  Use the Call Stack window to find the calling function and navigate to its source code. For more information, see [How to: Use the Call Stack Window](../vs140/How-to--Use-the-Call-Stack-Window.md).  
  
## See Also  
 [Debugging Native Code FAQs](../vs140/Debugging-Native-Code-FAQs.md)   
 [Breakpoints](assetId:///fe4eedc1-71aa-4928-962f-0912c334d583)   
 [Debugging Native Code](../vs140/Debugging-Native-Code.md)