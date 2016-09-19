---
title: "Thread-Specific Hot Keys"
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
ms.assetid: b6021274-1498-483f-bcbf-ba5723547cc8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Thread-Specific Hot Keys
An application sets a thread-specific hot key ([CHotKeyCtrl](../vs140/CHotKeyCtrl-Class.md)) by using the Windows **RegisterHotKey** function. When the user presses a thread-specific hot key, Windows posts a [WM_HOTKEY](http://msdn.microsoft.com/library/windows/desktop/ms646279) message to the beginning of a particular thread's message queue. The **WM_HOTKEY** message contains the virtual key code, shift state, and user-defined ID of the specific hot key that was pressed. For a list of standard virtual key codes, see Winuser.h. For more information on this method, see [RegisterHotKey](http://msdn.microsoft.com/library/windows/desktop/ms646309).  
  
 Note that the shift state flags used in the call to **RegisterHotKey** are not the same as those returned by the [GetHotKey](../vs140/CHotKeyCtrl--GetHotKey.md) member function; you'll have to translate these flags before calling **RegisterHotKey**.  
  
## See Also  
 [Using CHotKeyCtrl](../vs140/Using-CHotKeyCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)