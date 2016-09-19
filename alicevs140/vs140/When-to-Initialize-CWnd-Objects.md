---
title: "When to Initialize CWnd Objects"
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
ms.assetid: 4d31bcb1-73db-4f2f-b71c-89b087569a10
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# When to Initialize CWnd Objects
You cannot create your own child windows or call any Windows API functions in the constructor of a `CWnd`-derived object. This is because the `HWND` for the `CWnd` object has not been created yet. Most Windows-specific initialization, such as adding child windows, must be done in an [OnCreate](../vs140/CWnd--OnCreate.md) message handler.  
  
## What do you want to know more about?  
  
-   [Creating document frame windows](../vs140/Creating-Document-Frame-Windows.md)  
  
-   [Document/view creation](../vs140/Document-View-Creation.md)  
  
## See Also  
 [Using Frame Windows](../vs140/Using-Frame-Windows.md)