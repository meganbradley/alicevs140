---
title: "Allocating and Deallocating Window Memory"
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
ms.assetid: 7c962539-8461-4846-b5ca-fe3b15c313dc
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Allocating and Deallocating Window Memory
Do not use the C++ **delete** operator to destroy a frame window or view. Instead, call the `CWnd` member function `DestroyWindow`. Frame windows, therefore, should be allocated on the heap with operator **new**. Be careful when allocating frame windows on the stack frame or globally. Other windows should be allocated on the stack frame whenever possible.  
  
## What do you want to know more about?  
  
-   [Creating windows](../vs140/Creating-Windows.md)  
  
-   [Window destruction sequence](../vs140/Window-Destruction-Sequence.md)  
  
-   [Detaching a CWnd from its HWND](../vs140/Detaching-a-CWnd-from-Its-HWND.md)  
  
## See Also  
 [Destroying Window Objects](../vs140/Destroying-Window-Objects.md)