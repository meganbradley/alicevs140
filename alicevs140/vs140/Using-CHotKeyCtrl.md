---
title: "Using CHotKeyCtrl"
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
ms.assetid: 9b207117-d848-4224-8888-c3d197bb0c95
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using CHotKeyCtrl
A hot key control, represented by class [CHotKeyCtrl](../vs140/CHotKeyCtrl-Class.md), is a window that displays a text representation of the key combination the user types into it, such as CTRL+SHIFT+Q. It also maintains an internal representation of this key in the form of a virtual key code and a set of flags that represent the shift state. The hot key control does not actually set the hot key — doing that is up to your program. (For a list of standard virtual key codes, see Winuser.h.)  
  
 Use a hot key control to get a user's input for which hot key to associate with a window or thread. Hot key controls are often used in dialog boxes, such as you might display when asking the user to assign a hot key. It is your program's responsibility to retrieve the values describing the hot key from the hot key control and to call the appropriate functions to associate the hot key with a window or thread.  
  
## What do you want to know more about?  
  
-   [Using a Hot Key Control](../vs140/Using-a-Hot-Key-Control.md)  
  
-   [Setting a Hot Key](../vs140/Setting-a-Hot-Key.md)  
  
-   [Global Hot Keys](../vs140/Global-Hot-Keys.md)  
  
-   [Thread-Specific Hot Keys](../vs140/Thread-Specific-Hot-Keys.md)  
  
## See Also  
 [Controls (MFC)](../vs140/Controls--MFC-.md)