---
title: "Frame Window Classes (Windows)"
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
ms.assetid: 6342ec5f-f922-4da8-a78e-2f5f994c7142
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Frame Window Classes (Windows)
Frame windows are windows that frame an application or a part of an application. Frame windows usually contain other windows, such as views, tool bars, and status bars. In the case of `CMDIFrameWnd`, they may contain `CMDIChildWnd` objects indirectly.  
  
 [CFrameWnd](../vs140/CFrameWnd-Class.md)  
 The base class for an SDI application's main frame window. Also the base class for all other frame window classes.  
  
 [CMDIFrameWnd](../vs140/CMDIFrameWnd-Class.md)  
 The base class for an MDI application's main frame window.  
  
 [CMDIChildWnd](../vs140/CMDIChildWnd-Class.md)  
 The base class for an MDI application's document frame windows.  
  
 [CMiniFrameWnd](../vs140/CMiniFrameWnd-Class.md)  
 A half-height frame window typically seen around floating toolbars.  
  
 [COleIPFrameWnd](../vs140/COleIPFrameWnd-Class.md)  
 Provides the frame window for a view when a server document is being edited in place.  
  
## Related Class  
 Class `CMenu` provides an interface through which to access your application's menus. It is useful for manipulating menus dynamically at run time; for example, when adding or deleting menu items according to context. Although menus are most often used with frame windows, they can also be used with dialog boxes and other nonchild windows.  
  
 [CMenu](../vs140/CMenu-Class.md)  
 Encapsulates an `HMENU` handle to the application's menu bar and pop-up menus.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)