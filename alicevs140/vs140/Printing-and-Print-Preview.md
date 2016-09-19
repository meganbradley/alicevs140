---
title: "Printing and Print Preview"
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
ms.assetid: d15059cd-32de-4450-95f7-e73aece238f6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Printing and Print Preview
MFC supports printing and print preview for your program's documents via class [CView](../vs140/CView-Class.md). For basic printing and print preview, simply override your view class's [OnDraw](../vs140/CView--OnDraw.md) member function, which you must do anyway. That function can draw to the view on the screen, to a printer device context for an actual printer, or to a device context that simulates your printer on the screen.  
  
 You can also add code to manage multipage document printing and preview, to paginate your printed documents, and to add headers and footers to them.  
  
 This family of articles explains how printing is implemented in the Microsoft Foundation Class Library (MFC) and how to take advantage of the printing architecture already built into the framework. The articles also explain how MFC supports easy implementation of print preview functionality and how you can use and modify that functionality.  
  
## What do you want to know more about?  
  
-   [Printing](../vs140/Printing.md)  
  
-   [Print preview architecture](../vs140/Print-Preview-Architecture.md)  
  
-   [Sample](../vs140/Visual-C---Samples.md)  
  
## See Also  
 [User Interface Elements](../vs140/User-Interface-Elements--MFC-.md)