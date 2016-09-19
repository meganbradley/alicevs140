---
title: "Using a Window"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b3b9cc8e-4287-486b-b080-38852bc2943a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using a Window
Class [CWindow](../vs140/CWindow-Class.md) allows you to use a window. Once you attach a window to a `CWindow` object, you can then call `CWindow` methods to manipulate the window. `CWindow` also contains an `HWND` operator to convert a `CWindow` object to an `HWND`. Thus you can pass a `CWindow` object to any function that requires a handle to a window. You can easily mix `CWindow` method calls and Win32 function calls, without creating any temporary objects.  
  
 Because `CWindow` has only two data member (a window handle and the default dimensions), it does not impose an overhead on your code. In addition, many of the `CWindow` methods simply wrap corresponding Win32 API functions. By using `CWindow`, the `HWND` member is automatically passed to the Win32 function.  
  
 In addition to using `CWindow` directly, you can also derive from it to add data or code to your class. ATL itself derives three classes from `CWindow`: [CWindowImpl](../vs140/Implementing-a-Window.md), [CDialogImpl](../vs140/Implementing-a-Dialog-Box.md), and [CContainedWindowT](../vs140/Using-Contained-Windows.md).  
  
## See Also  
 [Window Classes](../vs140/ATL-Window-Classes.md)