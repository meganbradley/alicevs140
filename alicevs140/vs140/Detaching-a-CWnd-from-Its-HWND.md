---
title: "Detaching a CWnd from Its HWND"
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
ms.assetid: 6efadf84-0517-4a3f-acfd-216e088f19c6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Detaching a CWnd from Its HWND
If you need to circumvent the object-`HWND` relationship, MFC provides another `CWnd` member function, [Detach](../vs140/CWnd--Detach.md), which disconnects the C++ window object from the Windows window. This prevents the destructor from destroying the Windows window when the object is destroyed.  
  
## What do you want to know more about?  
  
-   [Creating windows](../vs140/Creating-Windows.md)  
  
-   [Window destruction sequence](../vs140/Window-Destruction-Sequence.md)  
  
-   [Allocating and deallocating window memory](../vs140/Allocating-and-Deallocating-Window-Memory.md)  
  
## See Also  
 [Window Objects](../vs140/Window-Objects.md)