---
title: "Destroying Window Objects"
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
ms.assetid: 3241fea0-c614-4a25-957d-20f21bd5fd0c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Destroying Window Objects
Care must be taken with your own child windows to destroy the C++ window object when the user is finished with the window. If these objects are not destroyed, your application will not recover their memory. Fortunately, the framework manages window destruction as well as creation for frame windows, views, and dialog boxes. If you create additional windows, you are responsible for destroying them.  
  
## What do you want to know more about?  
  
-   [Window destruction sequence](../vs140/Window-Destruction-Sequence.md)  
  
-   [Allocating and deallocating window memory](../vs140/Allocating-and-Deallocating-Window-Memory.md)  
  
-   [Detaching a CWnd from its HWND](../vs140/Detaching-a-CWnd-from-Its-HWND.md)  
  
-   [General Window Creation Sequence](../vs140/General-Window-Creation-Sequence.md)  
  
-   [Destroying frame windows](../vs140/Destroying-Frame-Windows.md)  
  
## See Also  
 [Window Objects](../vs140/Window-Objects.md)