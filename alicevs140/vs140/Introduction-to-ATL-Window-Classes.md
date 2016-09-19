---
title: "Introduction to ATL Window Classes"
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
ms.assetid: 503efc2c-a269-495d-97cf-3fb300d52f3d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Introduction to ATL Window Classes
The following ATL classes are designed to implement and manipulate windows:  
  
-   [CWindow](../vs140/CWindow-Class.md) allows you to attach a window handle to the `CWindow` object. You then call `CWindow` methods to manipulate the window.  
  
-   [CWindowImpl](../vs140/CWindowImpl-Class.md) allows you to implement a new window and process messages with a message map. You can create a window based on a new Windows class, superclass an existing class, or subclass an existing window.  
  
-   [CDialogImpl](../vs140/CDialogImpl-Class.md) allows you to implement a modal or a modeless dialog box and process messages with a message map.  
  
-   [CContainedWindowT](../vs140/CContainedWindowT-Class.md) is a prebuilt class that implements a window whose message map is contained in another class. Using `CContainedWindowT` allows you to centralize message processing in one class.  
  
-   [CAxDialogImpl](../vs140/CAxDialogImpl-Class.md) allows you to implement a dialog box (modal or modeless) that hosts ActiveX controls.  
  
-   [CSimpleDialog](../vs140/CSimpleDialog-Class.md) allows you to implement a modal dialog box with basic functionality.  
  
-   [CAxWindow](../vs140/CAxWindow-Class.md) allows you to implement a window that hosts an ActiveX control.  
  
-   [CAxWindow2T](../vs140/CAxWindow2T-Class.md) allows you to implement a window that hosts a licensed ActiveX control.  
  
 In addition to specific window classes, ATL provides several classes designed to make the implementation of an ATL window object easier. They are as follows:  
  
-   [CWndClassInfo](../vs140/CWndClassInfo-Class.md) manages the information of a new window class.  
  
-   [CWinTraits](../vs140/CWinTraits-Class.md) and [CWinTraitsOR](../vs140/CWinTraitsOR-Class.md) provide a simple method of standardizing the traits of an ATL window object.  
  
## See Also  
 [Window Classes](../vs140/ATL-Window-Classes.md)