---
title: "Windows Support Classes"
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
ms.assetid: 750b14d5-d787-4d2b-9728-ac199ccad489
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Windows Support Classes
The following classes provide support for windows:  
  
-   [_U_MENUorID](../vs140/_U_MENUorID-Class.md) Provides wrappers for **CreateWindow** and **CreateWindowEx**.  
  
-   [CWindow](../vs140/CWindow-Class.md) Contains methods for manipulating a window. `CWindow` is the base class for `CWindowImpl`, `CDialogImpl`, and `CContainedWindow`.  
  
-   [CWindowImpl](../vs140/CWindowImpl-Class.md) Implements a window based on a new window class. Also allows you to subclass or superclass the window.  
  
-   [CDialogImpl](../vs140/CDialogImpl-Class.md) Implements a dialog box.  
  
-   [CAxDialogImpl](../vs140/CAxDialogImpl-Class.md) Implements a dialog box (modal or modeless) that hosts ActiveX controls.  
  
-   [CSimpleDialog](../vs140/CSimpleDialog-Class.md) Implements a dialog box (modal or modeless) with basic functionality.  
  
-   [CAxWindow](../vs140/CAxWindow-Class.md) Manipulates a window that hosts an ActiveX control.  
  
-   [CAxWindow2T](../vs140/CAxWindow2T-Class.md) Provides methods for manipulating a window that hosts an ActiveX control and also has support for hosting licensed ActiveX controls.  
  
-   [CContainedWindowT](../vs140/CContainedWindowT-Class.md) Implements a window contained within another object.  
  
-   [CWndClassInfo](../vs140/CWndClassInfo-Class.md) Manages the information of a new window class.  
  
-   [CDynamicChain](../vs140/CDynamicChain-Class.md) Supports dynamic chaining of message maps.  
  
-   [CMessageMap](../vs140/CMessageMap-Class.md) Allows an object to expose its message maps to other objects.  
  
-   [CWinTraits](../vs140/CWinTraits-Class.md) Provides a simple method of standardizing the traits of an ATL window object.  
  
-   [CWinTraitsOR](../vs140/CWinTraitsOR-Class.md) Provides default values for window styles and extended styles used to create a window. These values are added, using the logical-OR operator, to values provided during the creation of a window.  
  
## Related Articles  
 [ATL Window Classes](../vs140/ATL-Window-Classes.md)  
  
 [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md)  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Window Class Macros](../vs140/Window-Class-Macros.md)